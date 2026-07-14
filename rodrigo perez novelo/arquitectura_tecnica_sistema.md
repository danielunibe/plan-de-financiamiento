# Arquitectura Técnica del Ecosistema Bio-IA
## *Especificación de Sistema Local-First y Procesamiento en el Borde*

Este documento describe la arquitectura de software, el flujo de datos y la integración del stack tecnológico de **Daniel Alexis Aguilar Unibe** para implementar el ecosistema **Mocell AI-Edge / BioChain Link**. La arquitectura está optimizada para la privacidad de datos clínicos, bajo consumo de recursos (OPEX mínimo) y rendimiento de baja latencia.

---

## 1. Diagrama General de Arquitectura Lógica

El sistema se compone de una aplicación de escritorio nativa (**Tauri v2**) instalada en las clínicas/laboratorios, conectada a una base de datos local y a motores de inferencia de IA en local (de ser posible) con fallback a la nube.

```
       ┌─────────────────────────────────────────────────────────────┐
       │                 CLIENTE (Frontend React 19)                 │
       │  - UI Glassmorphic (MySoul Design)                          │
       │  - Visualizador 3D (Three.js / Canvas 2D de Órbitas)        │
       │  - Captura de Voz & Audio Visualizer (Web Audio API)        │
       │  - Adaptabilidad por Container Queries                      │
       └──────────────────────────────┬──────────────────────────────┘
                                      │
                         IPC (Inter-Process Comm.)
                                      │
       ┌──────────────────────────────▼──────────────────────────────┐
       │                NÚCLEO NATIVO (Tauri v2 / Rust)              │
       │  - Manejo de Ventana Transparente / Acrílica                │
       │  - Cifrado de Archivos y Seguridad Local (AES-GCM)          │
       │  - Comunicación por Named Pipes con C# (.NET)               │
       │  - Orquestador de Tareas en Segundo Plano                   │
       └─────┬────────────────────────┬────────────────────────┬─────┘
             │                        │                        │
             ▼                        ▼                        ▼
     ┌───────────────┐        ┌───────────────┐        ┌───────────────┐
     │ BASE DE DATOS │        │  IA LOCAL /   │        │ MICROSERVICIO │
     │ LOCAL-FIRST   │        │ CONVERSACIONAL│        │   EDGE-AI     │
     │               │        │               │        │               │
     │ SQLite Core   │        │ Ollama Server │        │ Python (ONNX) │
     │ (Expedientes) │        │ (Llama/Gemma) │        │ (Detección y  │
     │               │        │               │        │ Segmentación  │
     │ Orama Indexer │        │ Kokoro TTS /  │        │   Celular)    │
     │ (Búsqueda Vec)│        │ Whisper.cpp   │        │               │
     └───────────────┘        └───────────────┘        └───────────────┘
```

---

## 2. Componentes del Ecosistema

### A. Capa de Presentación (Fidelity UI / 3D)
*   **Framework:** **React 19** + **TypeScript** + **Vite**. Permite el uso de Hooks reactivos avanzados para gestionar estados complejos de visualización.
*   **Estilo Visual:** Hoja de estilos basada en **Tailwind CSS 4** con el lenguaje de diseño **MySoul** (efectos de Glassmorphism avanzados mediante `backdrop-filter: blur()`, sombras y paletas de color Dreamcore con curvas extremas y profundidades espaciales de 16 capas).
*   **Motor 3D/Simulaciones:** Canvas HTML5 optimizado para renderizar las órbitas de pacientes y viales de **Synapse-Match** y visualizaciones WebGL con **Three.js** para el gemelo digital de **Bio-Simulacra 3D**.
*   **Adaptabilidad:** CSS **Container Queries** (`container-type: inline-size`) para empaquetar componentes lógicos independientes que se reordenan automáticamente al colapsar pantallas en interfaces de quirófano.

### B. Capa de Control y Seguridad Nativa (Tauri Core)
*   **Core:** **Rust 2021** (Tauri v2). Rust proporciona seguridad de memoria y un consumo de recursos sumamente bajo.
*   **B Vault (Seguridad):** Encriptación simétrica local **AES-GCM-256** utilizando llaves derivadas de forma segura mediante **Argon2** para garantizar que los expedientes de sueroterapia y medicina funcional estén seguros en local, cumpliendo con la legislación COFEPRIS y de protección de datos.
*   **Integración de Voz:** Enlace directo de audio con **Web Audio API** en el frontend que envía datos de buffer de audio al backend para transcripción inmediata mediante **Whisper.cpp**.

### C. Motores de Inferencia (AI Engine Layer)
*   **Segmentación Celular (Sentinel AI):** Microservicio local en **Python** que carga un modelo de segmentación de imágenes **ONNX** optimizado para CPU. Se conecta mediante WebSockets o gRPC local a Tauri para recibir los cuadros de video del microscopio y responder con los polígonos de delimitación celular.
*   **Lógica de Voz (Neuro-Lumina):** Inferencia conversacional local consumiendo un modelo de lenguaje de la familia **Gemma 4** a través del endpoint local de **Ollama**. La síntesis de voz final se genera localmente invocando un servidor HTTP local de **Kokoro TTS**.
*   **Búsqueda Híbrida Vectorial:** Motor de búsqueda **Orama** corriendo localmente en el cliente para calcular similitudes biológicas instantáneas entre expedientes e inventarios celulares de **Synapse-Match**.

---

## 3. Flujo de Datos Críticos

### Escenario: Proceso de Certificación de Lote (Laboratorio)
1.  El microscopio óptico enfoca la placa de cultivo de células madre.
2.  La cámara del smartphone captura el flujo de video y lo transmite a la app de escritorio Tauri.
3.  El núcleo de Tauri transfiere los frames al worker local de Python con el modelo ONNX.
4.  El modelo ONNX calcula la confluencia celular y la tasa de senescencia.
5.  El frontend React renderiza en tiempo real los contornos fluorescentes (verde, amarillo, rojo).
6.  Al finalizar el análisis, Tauri escribe los metadatos de viabilidad en la base de datos **SQLite** local, genera una firma hash criptográfica inmutable y actualiza el servicio de **BioChain Nexus** mediante un webhook de **n8n** para imprimir el código QR dinámico.
