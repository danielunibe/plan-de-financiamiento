# Arquitectura Técnica del Ecosistema Notaría AI-Edge
## *Especificación de Sistema Local-First y Procesamiento en el Borde*

Este documento describe la arquitectura de software, el flujo de datos y la integración del stack tecnológico de **Daniel Alexis Aguilar Unibe** para implementar el ecosistema **Notaría AI-Edge / LexChain Link**. La arquitectura está optimizada para la estricta privacidad de datos legales y escrituras, bajo consumo de recursos (OPEX mínimo) y rendimiento de baja latencia offline.

---

## 1. Diagrama General de Arquitectura Lógica

El sistema se compone de una aplicación de escritorio nativa (**Tauri v2**) instalada en las computadoras de la notaría, conectada a una base de datos local y a motores de inferencia de IA locales que resguardan la seguridad de la información.

```
       ┌─────────────────────────────────────────────────────────────┐
       │                 CLIENTE (Frontend React 19)                 │
       │  - UI Glassmorphic (MySoul Design & Bento Grid)             │
       │  - Visualizador de Escrituras (Canvas 2D / Three.js)        │
       │  - Captura de Voz & Audio Visualizer (Web Audio API)        │
       │  - Adaptabilidad por Container Queries                      │
       └──────────────────────────────┬──────────────────────────────┘
                                      │
                          IPC (Inter-Process Comm.)
                                      │
       ┌──────────────────────────────▼──────────────────────────────┐
       │                NÚCLEO NATIVO (Tauri v2 / Rust)              │
       │  - Manejo de Ventanas de Firma e Interfaz Acrílica          │
       │  - Cifrado de Escrituras y Documentos (AES-GCM)             │
       │  - Comunicación por Named Pipes con C# (.NET)               │
       │  - Orquestador de Tareas y Resguardo Local                  │
       └─────┬────────────────────────┬────────────────────────┬─────┘
             │                        │                        │
             ▼                        ▼                        ▼
     ┌───────────────┐        ┌───────────────┐        ┌───────────────┐
     │ BASE DE DATOS │        │  IA LOCAL /   │        │ MICROSERVICIO │
     │ LOCAL-FIRST   │        │ CONVERSACIONAL│        │   EDGE-AI     │
     │               │        │               │        │               │
     │ SQLite Core   │        │ Ollama Server │        │ Python (ONNX) │
     │ (Escrituras)  │        │ (Llama/Gemma) │        │ (Detección de │
     │               │        │               │        │   Firmas y    │
     │ Orama Indexer │        │ Kokoro TTS /  │        │   Cotejo)     │
     │ (Búsqueda Vec)│        │ Whisper.cpp   │        │               │
     └───────────────┘        └───────────────┘        └───────────────┘
```

---

## 2. Componentes del Ecosistema

### A. Capa de Presentación (Fidelity UI / Interactive WebGL)
*   **Framework:** **React 19** + **TypeScript** + **Vite**. Gestiona los estados interactivos del visor de contratos y la interfaz del notario.
*   **Estilo Visual:** Hoja de estilos basada en **Tailwind CSS 4** implementando el lenguaje de diseño **MySoul** (efectos de Glassmorphism avanzados con `backdrop-filter: blur()`, sombras y paletas de color Bento Grid con tipografía moderna y transiciones fluidas a 60 FPS).
*   **Motor Interactivo:** Canvas HTML5 para representar la búsqueda orbital de escrituras de **LexiMap** y WebGL con **Three.js** para renderizar los nodos de cláusulas interactivas en la pantalla de firmas.
*   **Adaptabilidad:** CSS **Container Queries** (`container-type: inline-size`) que garantizan que el visor y HUD de firmas mantengan legibilidad y control óptimo sin importar el dispositivo (tablet o pantalla de firma dedicada).

### B. Capa de Control y Seguridad Nativa (Tauri Core)
*   **Core:** **Rust 2021** (Tauri v2). Rust proporciona estabilidad de memoria y un consumo de recursos sumamente bajo, ideal para correr de fondo en la notaría (<1% CPU).
*   **Cripto-Bóveda (Seguridad):** Encriptación simétrica local **AES-GCM-256** utilizando llaves derivadas de forma segura mediante **Argon2** para garantizar que los expedientes notariales, identificaciones escaneadas y borradores de escrituras permanezcan protegidos en local, cumpliendo estrictamente con la Ley General de Protección de Datos Personales en Posesión de Particulares.
*   **Integración de Voz:** Enlace directo de audio con **Web Audio API** en el frontend que envía datos de buffer de audio al backend para transcripción inmediata mediante **Whisper.cpp**.

### C. Motores de Inferencia (AI Engine Layer)
*   **Detección y Cotejo de Firmas (Sentinel AI):** Microservicio local en **Python** que carga un modelo de segmentación de imágenes **ONNX** optimizado para CPU. Se conecta mediante WebSockets o gRPC local a Tauri para recibir las imágenes capturadas de las firmas y responder con los polígonos de delimitación y porcentaje de coincidencia.
*   **Asistente Lex-Lumina (Voz Local):** Inferencia conversacional local consumiendo un modelo de lenguaje de la familia **Gemma 4** a través de **Ollama**. La síntesis de voz final se genera localmente invocando un servidor HTTP local de **Kokoro TTS**.
*   **Búsqueda Semántica:** Motor de búsqueda **Orama** corriendo localmente en el cliente para calcular relaciones instantáneas en el historial de escrituras indexadas en **LexiMap**.

---

## 3. Flujo de Datos Críticos

### Escenario: Validación y Cotejo de Firma en Sala de Firmas
1.  El cliente firma físicamente una página de la escritura en la mesa de firmas.
2.  La cámara cenital captura el cuadro de la firma física y lo transmite a la app de escritorio Tauri.
3.  El núcleo de Tauri transfiere los frames al worker local de Python con el modelo ONNX.
4.  El modelo ONNX detecta la firma, realiza el cotejo contra la credencial INE/Pasaporte previamente cargada y calcula el nivel de coincidencia.
5.  El frontend React renderiza en tiempo real el contorno verde (coincidencia segura) o rojo (alerta de discrepancia).
6.  Al finalizar el acto, Tauri escribe los metadatos de validación y el hash de la escritura en la base de datos **SQLite** local, genera una firma hash criptográfica inmutable y actualiza el servicio de **LexChain Nexus** mediante un webhook de **n8n** para imprimir el código QR dinámico de validación.
