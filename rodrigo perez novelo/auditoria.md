# Auditoría Integral de Carpetas de Desarrollo y Proyectos

**Fecha de Análisis:** Junio 2026  
**Auditor:** Antigravity AI Engine  
**Objetivo:** Clasificar el ecosistema de carpetas locales y de respaldo, separando los proyectos de software consolidados y activos de los archivos basura, temporales o históricos para optimizar el espacio de trabajo.

---

## 📊 Resumen Ejecutivo del Ecosistema

El ecosistema digital analizado abarca dos grandes áreas:
1. **Entorno de Trabajo Local:** 18 directorios que contienen proyectos activos basados en tecnologías web y de escritorio modernas (React, Tauri, Rust, Next.js, .NET 8, Python).
2. **Entorno de Respaldo Voyager:** Un archivo histórico y conceptual de 63 proyectos, que documenta la visión del producto, marcas, prototipos visuales y de videojuegos.

### Cuadro General de Clasificación (Entorno Local)

| Directorio | Clasificación | Stack Tecnológico Principal | Estado de Madurez | Acción Recomendada |
| :--- | :--- | :--- | :--- | :--- |
| **1JuliaDEV** (dentro de julia) | ✅ Proyecto Activo | Tauri, Rust, React, Tailwind CSS | MVP Funcional (Escritorio) | **Conservar en Workspace** |
| **app vivo** | ✅ Proyecto Activo | Next.js, Capacitor, React | Aplicación Móvil en Desarrollo | **Conservar en Workspace** |
| **ethyria-app** | ✅ Proyecto Activo | Tauri, Rust, React, Vite | Asistente de IA Offline | **Conservar en Workspace** |
| **Reactbite** | ✅ Proyecto Activo | React 19, Vite, Host Runtime | Micro-App Container Runtime | **Conservar en Workspace** |
| **nodia** | ✅ Proyecto Activo | React, UX/UI, Agent Specs | Orquestador de Agentes IA | **Conservar en Workspace** |
| **Master dev click switch swiss** | ✅ Proyecto Activo | .NET 8, Tauri, Rust, Python | OS Workflow Automation | **Conservar en Workspace** |
| **Retriver** | ✅ Proyecto Activo | Python, SQLite, Mem0 Sim | Simulador de Memoria Semántica | **Conservar en Workspace** |
| **pulsar-project** | ✅ Proyecto Activo | Tauri, Rust, Python Workers | Suite de Procesamiento de Imagen | **Conservar en Workspace** |
| **21_Pixvoxia** | 🎨 Diseño y UX | Blueprints, iOS UI, Canvas | Diseño de Interfaz Móvil | **Conservar en Workspace** |
| **TSK DISENO** | 🎨 Diseño y UX | React, TDAH App Blueprints | Diseño y Prototipo Funcional | **Conservar en Workspace** |
| **desarrollo web unova games studio** | 📄 Documental/Marca | Branding Briefs, Web Assets | Dossier de Identidad Corporativa | **Archivar en Carpeta de Diseños** |
| **nueva propuesta windows 12** | 📄 Documental/Diseño | HTML, Especificación Nano | Concepto de Usabilidad (Focus) | **Archivar en Documentos** |
| **Desarrollo CV borderlands3** | 🗂️ Repositorio Mixto | React, Tailwind, MP3, CVs | Portafolio Personal + UnibeLands-3 | **Conservar en Workspace** |
| **nodia-home-clone** | 📦 Recursos/Assets | Zip Low-Poly, Assets Gráficos | Assets de Soporte para Nodia | **Mover a Carpeta de Assets** |
| **Ethyria** (Capitalizado) | 🗂️ Copia y Respaldos | Logs, Documentación, Videos | Respaldo Histórico de Ethyria | **Mover a Respaldo Seguro** |
| **transparentimagen** | 🗂️ Respaldos/Sandbox | Backups de Asteria / Image Enhancer | Sandbox Antiguo de Segmentación | **Mover a Respaldo Seguro** |
| **tmp** | ❌ Basura Temporal | Logs de Caída, Logs PID, PNGs Temp | Basura del Sistema / Logs de Vite | **Eliminar de Inmediato** |
| **todos documentos** | ❌ Archivo Muerto | 91 Archivos de Texto (.txt) | Claude Logs y Apuntes Antiguos | **Archivar o Eliminar** |

---

## 🖥️ 1. Detalle del Entorno Local

A continuación, se detalla el análisis y diagnóstico de cada una de las carpetas ubicadas en el entorno local:

### 1.1. Proyectos Activos de Código Fuente (No Modificar / Conservar)

*   **app vivo:**
    *   **Propósito:** Aplicación móvil diseñada para la gestión comercial y guía de ventas.
    *   **Arquitectura:** Construida sobre Next.js y empaquetada con Capacitor para despliegue nativo en Android/iOS.
    *   **Estado:** Contiene la estructura lista para compilar, con carpetas de plataforma móvil y documentación interna de arquitectura.
    *   **Diagnóstico:** Proyecto prioritario. Conservar intacto en el entorno principal.

*   **ethyria-app:**
    *   **Propósito:** Repositorio principal de desarrollo del asistente de voz e inteligencia artificial local y offline (Ethyria).
    *   **Arquitectura:** React en el frontend, Tauri con Rust en el backend de escritorio, y servidor TTS de voz local.
    *   **Estado:** Entorno completamente funcional con variables locales de entorno configuradas y scripts de ejecución nativos.
    *   **Diagnóstico:** Es el núcleo del desarrollo del asistente offline. Mantener para pruebas y builds de producción.

*   **Reactbite:**
    *   **Propósito:** Framework y entorno de ejecución para micro-aplicaciones portátiles (Mini App Runtimes) autocontenidas.
    *   **Arquitectura:** React 19, empaquetado Vite, configuraciones de TypeScript, y dependencias node_modules listas para desarrollo.
    *   **Estado:** Proyecto consolidado con reportes de migración de arquitectura y runtime funcional para lanzar micro-apps.
    *   **Diagnóstico:** Componente de portafolio técnico de alto nivel. Mantener.

*   **nodia:**
    *   **Propósito:** Ecosistema para la orquestación de tareas inteligentes mediante agentes virtuales y paneles interactivos.
    *   **Arquitectura:** Prototipado web React, protocolos avanzados de diseño de interacción y blueprints de comportamiento de IA.
    *   **Estado:** Activo, con documentación detallada del protocolo de desarrollo de agentes locales.
    *   **Diagnóstico:** Muestra tu visión técnica sobre orquestación de sistemas de agentes. Conservar.

*   **pulsar-project:**
    *   **Propósito:** Módulo de procesamiento y mejora de imagen en local utilizando Tauri y workers en Python.
    *   **Arquitectura:** Backend nativo Rust/Tauri con integraciones de Python SDK y procesos de observabilidad.
    *   **Estado:** Código activo y estructura limpia sin la basura de copias de seguridad que solía tener.
    *   **Diagnóstico:** Código limpio y listo para compilación nativa. Conservar.

*   **Master dev click switch swiss:**
    *   **Propósito:** Automatización de flujos de trabajo del sistema operativo mediante un único botón del mouse, atajos y hot corners.
    *   **Arquitectura:** Integración multiplataforma que combina scripting en Python con interfaces de usuario en C# WPF, Tauri y scripts Lua.
    *   **Estado:** Activo, con scripts listos para hooks del ratón en bajo nivel.
    *   **Diagnóstico:** Proyecto de productividad altamente presentable y diferencial. Conservar.

*   **Retriver:**
    *   **Propósito:** Implementación local de un motor de recuperación de información semántica y simulación de memoria (estilo Mem0).
    *   **Arquitectura:** Scripts de Python estructurados y base de datos local SQLite para indexación semántica.
    *   **Estado:** Activo, con resumen ejecutivo del proyecto incluido.
    *   **Diagnóstico:** Demo técnica robusta que demuestra tus capacidades en el manejo de bases de datos vectoriales locales. Conservar.

*   **julia (Subcarpeta: 1JuliaDEV):**
    *   **Propósito:** Núcleo de desarrollo de Julia AI, el procesador semántico central y visualizador esférico estilo Júpiter.
    *   **Arquitectura:** React, TypeScript, Tailwind CSS, empaquetado Vite y Tauri (Rust).
    *   **Estado:** El proyecto de desarrollo más importante del workspace. Contiene código funcional, componentes de UI, servicios de procesamiento y assets de marca.
    *   **Diagnóstico:** **Proyecto Insignia.** Mantener como prioridad absoluta en el espacio de trabajo.

*   **Desarrollo CV borderlands3 (Subcarpeta: UnibeLands-3):**
    *   **Propósito:** Contiene CVs de diseño y el proyecto *UnibeLands-3*, una aplicación web interactiva con temática de videojuegos y reproductor musical.
    *   **Arquitectura:** React, Vite, Tailwind CSS y assets de audio MP3 integrados.
    *   **Estado:** Código funcional y dependencias configuradas con PNPM.
    *   **Diagnóstico:** Aunque el nombre de la carpeta principal suena antiguo, el subdirectorio `UnibeLands-3` contiene un proyecto web interactivo funcional de gran valor estético. Conservar.

---

### 1.2. Recursos de Diseño, Assets y Documentales (Archivar / Mover)

*   **21_Pixvoxia:**
    *   **Propósito:** Repositorio de diseño UX/UI de la aplicación móvil iOS de Pixvoxia.
    *   **Estado:** Pura documentación visual, lienzos de diseño y esquemas (blueprints). No tiene código de programación activo en la raíz.
    *   **Acción:** Mover a una carpeta consolidada de diseño de interfaces para evitar desordenar la zona de código activo.

*   **TSK DISENO:**
    *   **Propósito:** Blueprints y esquemas del proyecto de diseño y apoyo para TDAH (Proyectia TSK).
    *   **Estado:** Carpeta documental que contiene archivos de texto explicativos y subcarpetas de diseño conceptual de flujos de trabajo.
    *   **Acción:** Mover a la misma carpeta de diseño que *Pixvoxia*.

*   **desarrollo web unova games studio (Subcarpeta: unovagames_dossier):**
    *   **Propósito:** Branding, logotipo, naming y guías de estilo para Unova Games Studio.
    *   **Estado:** Documentación pura en formato Markdown. Sin código web activo en la raíz.
    *   **Acción:** Mover a la carpeta de respaldos de identidad corporativa de *Unova Games*.

*   **nueva propuesta windows 12:**
    *   **Propósito:** Investigación conceptual sobre interfaces de usuario avanzadas, específicamente enfocada en el diseño del "Modo Nano" y botones táctiles interactivos.
    *   **Estado:** Archivos HTML estáticos de prueba de botones y documentos explicativos Markdown.
    *   **Acción:** Conservar o archivar en documentos personales de investigación.

*   **nodia-home-clone:**
    *   **Propósito:** Assets visuales en 3D (archivos ZIP de entornos low-poly) y referencias estéticas de interfaz para el desarrollo visual de *nodia*.
    *   **Estado:** No tiene código ejecutable; es un almacén de archivos de recursos pesados.
    *   **Acción:** Descomprimir o mover a una carpeta centralizada de assets 3D para liberar espacio visible en tu workspace principal.

---

### 1.3. Respaldos Antiguos y Sandbox (Mover a Disco Externo o Archivo)

*   **Ethyria (Carpeta con mayúscula inicial):**
    *   **Propósito:** Copia antigua o respaldo del proyecto de desarrollo de Ethyria.
    *   **Estado:** Contiene archivos duplicados de especificaciones de estado, scripts antiguos y archivos de video MP4.
    *   **Acción:** Su presencia genera confusión con la carpeta activa `ethyria-app`. Se recomienda mover esta versión antigua a tu unidad de respaldo seguro para mantener una sola versión activa.

*   **transparentimagen:**
    *   **Propósito:** Entorno antiguo utilizado como sandbox para entrenar e integrar segmentación de imágenes (modelos Asteria / Image Enhancer).
    *   **Estado:** Contiene más de 30 subcarpetas de copias de seguridad de Codex (`_codex_backup_*`) que ocupan espacio. La integración limpia y refinada de estas herramientas ya se encuentra en `pulsar-project`.
    *   **Acción:** Respaldo muerto. Mover a la unidad de almacenamiento externo para limpieza del disco local.

---

### 1.4. Archivos Basura y Temporales (Eliminar de forma Segura)

*   **tmp:**
    *   **Propósito:** Carpeta de desbordamiento de ejecuciones locales.
    *   **Estado:** Registros de errores de desarrollo (`ethyria-tauri-err.log`), capturas de pantalla de diagnósticos de UI, y archivos de ID de procesos (.pid) ya cerrados.
    *   **Acción:** **Basura digital.** Es 100% seguro vaciar o eliminar esta carpeta completa para eliminar ruido del sistema de compilación.

*   **todos documentos:**
    *   **Propósito:** Historial de notas, copias de chats de Claude / ChatGPT y apuntes antiguos sobre Julia y Júpiter.
    *   **Estado:** 91 archivos de texto `.txt` desordenados con texto plano copiado. No hay código ejecutable ni assets gráficos estructurados.
    *   **Acción:** Mover estos archivos de texto a una carpeta consolidada en la nube (como Google Drive) en una sección de "Apuntes Históricos" y eliminarlos del entorno local de programación.

---

## 💾 2. Análisis del Entorno de Respaldo (Unidad Voyager)

El disco de respaldo **Voyager** funciona como el archivo histórico y portafolio conceptual definitivo de tus ideas. No es un entorno de desarrollo activo en el día a día, pero contiene activos intelectuales de enorme valor. 

Los tres focos clave de código e ideas en este disco de respaldo son:

### 2.1. Sovereign Lab (SOVEREIGN_LAB)
*   **Propósito:** Entorno experimental local para la orquestación e integración de modelos de lenguaje offline (LLMs locales).
*   **Contenido:** Scripts de PowerShell para automatización de la pila de IA (`LLM-AutoManager.ps1`), scripts de despliegue y un agente local en Python (`local_agent.py`).
*   **Diagnóstico:** Tu "laboratorio offline". Contiene herramientas sumamente útiles de integración con Ollama. Conservar como repositorio de scripts útiles.

### 2.2. Unova Games
*   **Propósito:** Repositorio corporativo y de branding para el estudio de videojuegos Unova Games.
*   **Contenido:** 
    *   Actas constitutivas de sociedad en Word (`Acta - UNOVA - final.docx`) y presupuestos financieros en PDF.
    *   Diseños vectoriales de alta gama en Adobe Illustrator (.ai) y Photoshop (.psd) con el logotipo oficial, organigrama y credenciales.
    *   Estructuras web de presentación de landing pages en HTML de la sección héroe del sitio web de Unova.
*   **Diagnóstico:** Carpeta empresarial. Contiene el core de marca de tu estudio. Conservar intacta.

### 2.3. Proyectos Personales 2026 (proyectos voyager)
Esta carpeta aloja una base de conocimientos en Markdown y Obsidian que contiene la especificación y diseño detallado de **63 proyectos históricos y conceptuales**.
Los proyectos más significativos que demuestran capacidades sólidas de desarrollo y diseño de producto son:

1.  **Dragón Alebrije (Categoría Juegos de Mesa):** Juego de mesa de cartas físicas estructurado en base a la mitología mexicana. Cuenta con un documento de diseño de 8KB, distribución de 169 cartas y una versión de aplicación digital en desarrollo (`game-app`) escrita en Python y HTML/CSS.
2.  **Proyectia (Categoría Desktop):** Command center de alto rendimiento nativo para la administración masiva de tareas complejas de ingeniería. Estructura masiva de desarrollo en Rust/Tauri con frontend en React 19 y Framer Motion.
3.  **SereneSymphony (Categoría Desktop):** Solución completa en C# .NET y WPF orientada a la optimización estética y del rendimiento de Windows, que incluye el motor inteligente de gestión de ventanas *FlowDesk*.
4.  **ReflectIA (Categoría Desktop):** Prototipo avanzado en React y GSAP para simulación visual interactiva de físicas magnéticas, efectos reflectantes y Glassmorphism 3.0 en interfaces móviles.
5.  **ComedyClick (Categoría Desktop):** Concepto de "Cursor Líquido" de latencia ultra-baja en React 19 y Zustand, que convierte el puntero en un widget multifuncional.

---

## 🧼 3. Plan de Acción de Limpieza y Optimización

Para dejar tu espacio de trabajo de desarrollo local libre de desorden visual y optimizar el rendimiento de las búsquedas de tu IA asistente, realiza los siguientes pasos:

1.  **Eliminación Inmediata de Basura:**
    *   Elimina por completo la carpeta `tmp` (limpieza de logs de Vite/Tauri y dumps antiguos).
2.  **Consolidación Documental y Despeje de Workspace:**
    *   Crea una carpeta de respaldo llamada `_DOCUMENTACION_Y_DISENO` fuera de tu zona de proyectos de programación activos.
    *   Mueve a esta carpeta los directorios documentales: `21_Pixvoxia`, `TSK DISENO`, `desarrollo web unova games studio`, `nueva propuesta windows 12`, y `todos documentos`. Esto dejará solo proyectos que contengan código fuente ejecutable en tu workspace.
3.  **Gestión de Respaldos Muertos:**
    *   Mueve la carpeta antigua `Ethyria` (con mayúscula inicial) y la carpeta `transparentimagen` (sandbox antiguo) a tu disco de respaldo externo **Voyager 2026** o a una subcarpeta interna llamada `_ARCHIVADOS_` dentro de tu espacio local. Esto prevendrá que el software de desarrollo indexe código duplicado o logs de error antiguos.
4.  **Aislamiento de Assets Pesados:**
    *   Mueve `nodia-home-clone` a una sección de assets externos para no sobrecargar el repositorio activo de `nodia`.
