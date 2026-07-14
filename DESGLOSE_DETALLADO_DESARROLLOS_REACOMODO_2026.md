# Desglose detallado de desarrollos y reacomodo de datos 2026

**Fecha:** 17 de junio de 2026  
**Base de revisión:**  
- `G:\Otros ordenadores\AorusPC\Voyager 2026\Proyectos personales 2026\proyectos voyager`
- `C:\Desarrollos DEV daniel`
- Diagramas visuales compartidos por el usuario
- Inventario generado en `_analisis_reacomodo`

---

## 1. Propósito de este documento

Este documento no es un resumen de stack. Es un desglose de **qué contiene cada desarrollo**, qué tipo de activo representa, qué evidencia documental existe, cómo se conecta con el ecosistema Unova/Voyager y cómo debe reacomodarse para que sirva como base de inversión, ejecución y presentación.

La conclusión principal es:

> El ecosistema no debe verse como carpetas sueltas. Debe ordenarse como un portafolio con nodos centrales, productos financiables, activos técnicos base, IP creativa, backlog y archivo histórico.

---

## 2. Método de revisión aplicado

Se inventariaron los documentos Markdown útiles de ambos árboles.

| Origen | `.md` útiles detectados | Criterio |
|---|---:|---|
| Voyager | 1,335 | Documentación propia, fichas, PRD, roadmap, diseño, análisis, protocolos. |
| `C:\Desarrollos DEV daniel` | 1,562 | Documentación viva, auditorías, diseños, arquitectura, planes, historial útil. |
| Total revisado por inventario | 2,897 | Se excluyeron dependencias generadas, builds, cachés y documentación de terceros. |

Archivos generados para soporte del análisis:

| Archivo | Uso |
|---|---|
| `_analisis_reacomodo\voyager_md_files.txt` | Lista de `.md` detectados en Voyager. |
| `_analisis_reacomodo\c_dev_md_files.txt` | Lista de `.md` detectados en C. |
| `_analisis_reacomodo\md_doc_inventory.csv` | Inventario por archivo con señales de PRD, roadmap, diseño, arquitectura y riesgo. |
| `_analisis_reacomodo\project_doc_summary.csv` | Resumen agrupado por desarrollo/carpeta. |

---

## 3. Lectura del mapa visual proporcionado

Los diagramas muestran una arquitectura conceptual con estos ejes:

| Nodo visual | Lectura |
|---|---|
| **Unova games studio** | Nodo central de marca, estudio y portafolio. Debe funcionar como contenedor corporativo. |
| **VoyagerOS** | Eje de sistema operativo/interfaz. Agrupa herramientas de productividad, UX de sistema y módulos Windows. |
| **Apps** | Rama de aplicaciones móviles/web: Couplepay, Pixvoxia, Apartment22, Diaria, HilarIA, iPad Magic Pro, Punkpedia, PrismaCraft, EverythingUI. |
| **Herramientas azules** | Capa de sistema, IA, memoria y productividad: Julia, ReactBite, MySoul, Pulsaria, Voyager Files, Orbia, ComedyClick, Hyperpane, ReflectIA, Asteria. |
| **Proyectia** | Nodo de gestión/proyectos conectado al estudio. Debe tratarse como command center/productividad, no como simple app. |
| **Videojuegos / Juegos de mesa** | Rama creativa/IP: Neko Nesushi, Kaetso, Dragón Alebrije y otros mundos. |
| **Estrella** | Nodo puente conceptual. Parece representar el punto donde se cruzan IP, marca, producto y portafolio. |

Reacomodo recomendado:

```txt
Unova Studio
├─ 00_Gobernanza_y_Sociedad
├─ 01_Productos_Financiables
├─ 02_Activos_Tecnicos_Base
├─ 03_Portafolio_IP_Creativo
├─ 04_Backlog_Ordenado
└─ 05_Archivo_Historico_y_Evidencia
```

---

## 4. Desglose de carpetas activas en `C:\Desarrollos DEV daniel`

Estas carpetas son importantes porque reflejan lo que existe como trabajo local vivo, no solo como archivo histórico.

| Carpeta | Docs `.md` | Qué contiene realmente | Valor para inversión/desarrollo | Acción recomendada |
|---|---:|---|---|---|
| `Reactbite` | 108 | Runtime de micro-apps, docs de arquitectura, reparación, seguridad, permisos, `.rckbyte/.rbe`, Tauri/Rust/React. | Activo técnico base para empaquetar micro-herramientas y demos. | Mantener como proyecto canónico técnico. |
| `julia` | 89 | Sistema de conocimiento, metáfora de Sistema Solar, docs de negocio, UI/UX, seguridad, módulos de memoria. | Producto bandera para RAG local, conocimiento privado y pilotos B2B. | Prioridad alta para pilotos con Rodrigo/Eduardo. |
| `ethyria-app` | 8 | App local Tauri/React/Rust con TTS, estado de verdad, guardrails y arquitectura. | Módulo de IA conversacional/offline. | Conservar como base de interacción local-first. |
| `Ethyria` | 29 | Respaldo/documentación extendida de Ethyria, frontend, backend, audio, IA, comandos OS. | Archivo técnico y evidencia conceptual. | Usar como referencia, no como ruta canónica principal. |
| `nodia` | 70 | Orquestación de agentes, pipeline, PRD AAA, narrativa, despliegue, interfaz de nodos. | Plataforma emergente de agentes/automatización. | Preparar, pero pedir foco de usuario/mercado antes de vender. |
| `TSK DISENO` | 482 | Proyectia/Proyec[tdh]ia, TDAH, UI, mucha documentación histórica y duplicada. | Gran volumen de IP de productividad y UX cognitiva. | Separar activo vivo de `info vieja`; consolidar Proyectia TSK. |
| `Master dev click switch swiss` | 19 | Switch Click Swiss, documentación de arquitectura, packaging y plan estratégico. | Producto de interacción natural con potencial comercial Windows. | Candidato a producto vendible tras firma/certificado/QA. |
| `transparentimagen` | 258 | Asteria, image enhancer, roadmap, arquitectura, guardrails, sidecars Python. | IA visual local y workspace de procesamiento de imagen. | Mantener; no mezclar con Julia ni pilotos RAG. |
| `app vivo` | 70 | App móvil/asesor comercial, docs de APK, diseño, auditoría, estado e implementación. | Evidencia fuerte de entrega móvil y UX de ventas. | Usar como caso de producto comercial entregable. |
| `Retriver` | 305 | Bóveda de conocimiento, CV, PRDs, perfiles, memoria, análisis comercial y raw chats. | Archivo de inteligencia personal/comercial; posible CRM semántico. | Reacomodar como `05_Archivo_Historico_y_Evidencia` y extraer solo señal. |
| `21_Pixvoxia` | 13 | Canvas Pro, blueprint iOS, PRD de motor creativo. | Herramienta creativa pixel/voxel. | Mantener en backlog de apps creativas. |
| `desarrollo web unova games studio` | 9 | Dossier de marca, naming, web assets, identidad y brief web. | Fuente principal de marca Unova. | Mover a gobernanza/branding. |
| `Desarrollo CV borderlands3` | 51 | CV, perfil profesional, UnibeLands, deployment/readiness y portafolio. | Evidencia profesional de Daniel. | Separar CV/portafolio de productos. |
| `nueva propuesta windows 12` | 8 | Focus/Nano, investigación de UX Windows, iconos, modos de ventana. | Insumo para VoyagerOS/Focus/Nano. | Archivar como concepto UX de sistema. |
| `pulsar-project` | 2 | Proyecto Tauri/Rust/Python de procesamiento, docs mínimos detectados. | Activo técnico, pero con poca documentación Markdown visible. | Revisar código aparte si se prioriza. |
| `nodia-home-clone` | 15 | Clon/actualización de Nodia, docs de arquitectura e interfaz. | Referencia de estado visual. | Archivo de soporte, no canónico. |
| `plan de financiamiento` | 26 | Propuestas Rodrigo/Eduardo, auditoría, inversión, plan maestro. | Centro actual de estrategia/inversión. | Mantener como carpeta de negociación y documentos ejecutivos. |

---

## 5. Desglose Voyager - Software y sistemas

La categoría software es el núcleo tecnológico del ecosistema. Los documentos de sociedad Unova ya la dividen en clusters: gestión/comando, optimización del sistema, IA personal/datos y creatividad técnica.

| Desarrollo | Docs `.md` | Qué tiene | Estado documental | Papel en ecosistema | Acción |
|---|---:|---|---|---|---|
| **Proyectia / TSK** | C: 482, Voyager/sociedad | Command center, tareas, productividad, Octavia, TSK, gestión diaria y objetivos. | Muy alto, pero mezclado con histórico. | Producto prioritario de productividad. | Ejecutar ya si se consolida ruta viva. |
| **Switch Click Swiss** | Voyager 14 + C 19 | Interacción natural, macros, hooks, control Windows, documentación release-oriented. | Media/alta. | Producto power user. | Preparar para distribución. |
| **SereneSymphony** | 173 | Orquestación visual para Windows, blur, FlowDesk, automatización, WPF/.NET. | Muy alto, con mucho legacy duplicado. | Producto Windows premium. | Preparar tras limpieza de duplicados. |
| **Julia** | Voyager 1 + C 89 | Sistema de conocimiento, memoria visual orbital, RAG, privacidad local, docs de negocio. | Alto en C, bajo en Voyager directo. | Producto bandera B2B/conocimiento. | Prioridad alta. |
| **ReactBite** | Voyager 28 + C 108 | Runtime de micro-apps `.reactbite`, SDK, formato portátil, seguridad y empaquetado. | Muy alto. | Infraestructura base para demos y herramientas. | Activo técnico base. |
| **Ethyria** | Voyager 25 + C 37 | IA emocional, asistente local, voz, TTS, personalidad, offline-first. | Alto. | Capa de interacción/voz y narrativa IA. | Preparar, limitar alcance emocional. |
| **Nodia** | C 70 | Agentes, nodos, narrativa, automatización, PRD AAA. | Alto. | Orquestador futuro. | Preparar con usuario objetivo claro. |
| **Voyager Files** | 32 | Explorador de archivos semántico, iTagMe, IA tagging, UX de archivos. | Alto. | Satélite de Julia/Ethyria/VoyagerOS. | Preparar como módulo, no como producto inicial. |
| **Pulsar TikTok** | 29 | Descarga/transcripción/análisis de TikTok, conocimiento de contenido. | Medio/alto. | Ingesta de datos/contenido para Julia. | Preparar si hay caso comercial de creadores. |
| **Hyperpane** | 70 | Escritorio infinito, gestión visual de ventanas, docs de stack y módulos. | Alto. | UX de sistema/VoyagerOS. | Preparar; validar complejidad Windows. |
| **ReflectIA / ReplIA** | 44 | Simulación de lujo iPhone/AirPlay, UI premium, arquitectura y guías de compilación. | Alto. | Portafolio visual y posible herramienta nicho. | Pausar para no competir con B2B. |
| **FAAST** | 85 | Control gestual con Kinect/cámara, documentación técnica e interfaz. | Alto. | Hardware/accesibilidad/interacción natural. | Preparar como IP técnica. |
| **Slap!Faast** | 55 | Control del sistema, propuesta IA local, guías de instalación, modo Tony Stark. | Alto. | Interacción gestual/power tool. | Preparar o fusionar con FAAST. |
| **MySoul** | 43 | Identidad digital, estética Dreamcore/Glass, documentación de conciencia/espejo. | Alto, pero con backups. | Biblia estética/narrativa del ecosistema. | Usar como diseño/brand language. |
| **Debatia** | 13 | Debate multi-IA, deliberación con modelos/roles. | Medio. | SaaS conceptual IA. | Preparar solo si hay MVP simple. |
| **MaterialCode** | 14 | Editor nodal/IA para texturas 3D y materiales procedurales. | Medio. | Herramienta creativa/3D. | Pausar; valor de portafolio técnico. |
| **Panel-IA** | 14 | Orquestador tipo n8n local para PC. | Medio. | Automatización local. | Pausar hasta definir flujo real. |
| **PredictIA** | 14 | Clon de estilo de escritura personal. | Medio. | IA personal/productividad. | Preparar como módulo de Julia/Retriver. |
| **Quick Look App** | 13 | Previsualización tipo macOS para Windows con IA/metadatos. | Medio. | Utilidad Windows. | Preparar como quick win. |
| **ComedyClick** | Docs en Voyager + mapa | Cursor líquido/funcional, Magic Ring, interacción contextual. | Medio. | UX experimental de sistema. | Preparar como demo visual. |
| **WitchTricIA** | 13 | PowerShell con narrativa de hechicería para optimización PC. | Medio. | Tool de comunidad/branding. | Preparar ligero. |
| **VisualIA Suite** | 27 | Suite de modelos visuales, guías, templates, implementación IA visual. | Medio/alto. | IA generativa/visual. | Pausar hasta cerrar Asteria. |
| **TransfirIA** | 14 | Transferencia inteligente / AirPlay / flujo de datos. | Medio. | Módulo técnico. | Pausar. |
| **Windows A / VoyagerOS** | 16 + mapa | Sistema/UX Windows, shell, Focus/Nano, interfaz futura. | Medio. | Marco narrativo de OS. | Congelar como visión, no sprint. |
| **Orbia** | 13 | Visualización 3D de relaciones orbitantes. | Medio. | Satélite visual de Julia. | Congelar hasta que Julia cierre datos base. |
| **Interface New Prop Cerrar** | 13 | Microinteracción de cierre de ventanas. | Bajo/medio. | I+D visual. | Archivo UX. |
| **Traductor tiempo real** | 12 | Traducción integrada, posible fusión con ComedyClick. | Medio. | Feature satélite. | Fusionar, no producto separado. |

---

## 6. Desglose Voyager - Apps móviles/web

| Desarrollo | Docs `.md` | Qué tiene | Valor | Acción |
|---|---:|---|---|---|
| **Nutriflow** | 14 + C/relaciones | App para nutriólogos, seguimiento, visión computacional, PDFs reales. | HealthTech con cliente/uso real potencial. | Preparar. |
| **Volt-IA** | 15 | Auditoría eléctrica para México, React/TS/Gemini. | Nicho claro y problema entendible. | Preparar. |
| **Aparment22** | 15 | Búsqueda de departamentos con IA/scraping. | Dolor real, pero requiere scraping/proxies. | Preparar con cuidado legal. |
| **Pixvoxia** | C 13 + mapa | Canvas Pro pixel/voxel, motor creativo. | Herramienta creativa para juegos. | Backlog activo. |
| **HilarIA** | 14 | Artesanía de hilo/string art, patrones y posible 3D. | Producto creativo nicho. | Preparar ligero. |
| **SpeedDocumentAI** | 18 | Procesamiento ultra rápido de documentos, OCR/jobs. | Se conecta con RAG/Julia. | Preparar como módulo. |
| **Couplepay** | 14 | Finanzas de pareja. | Mercado B2C, pero sensible y competido. | Pausar. |
| **MedicIA** | 14 | Asistente preventivo salud. | Riesgo médico alto. | Pausar hasta definir límites. |
| **PrismaCraft** | 14 | Diseño/paletas/creatividad móvil. | Complemento creativo. | Pausar. |
| **Prompt-IA** | 14 | Biblioteca de prompts. | Útil como contenido, no gran producto. | Pausar. |
| **Punkped-IA / Punkpedia** | 14/15 | Enciclopedia/cultura alternativa. | IP/contenido. | Congelar. |
| **App Brainstorming** | 13 | Grafos semánticos móviles. | Se cruza con Julia/Nodia. | Congelar o fusionar. |
| **App David** | 12 | Asistente personal/microapp. | Puede servir para validación comercial. | Congelar hasta caso real. |
| **Juego inglés con IA** | 13 | EdTech gamificado. | Potencial, pero sin foco actual. | Congelar. |
| **Calculadora inteligente** | 14 | Calculadora/NLP, posible médica. | Riesgo/alcance difuso. | Congelar. |
| **iPad Magic Pro** | 14 | Suite táctil/productividad iPadOS. | Concepto UX. | Congelar. |
| **Nekiva** | 14 | Mascotas/lifestyle. | B2C sin tracción clara. | Congelar. |
| **Robtinator** | 14 | Simulación/agentes robóticos. | IP lúdica/técnica. | Congelar. |
| **UI Lab / Uiverse** | 13 | Laboratorio de microinteracciones. | Biblioteca de experimentos visuales. | Archivo de diseño. |
| **VitalIA** | 13 | Salud/bienestar. | Riesgo médico y scope amplio. | Congelar. |
| **Diaria** | mapa visual | Diario/productividad personal. | Puede fusionarse con MySoul/Julia. | No abrir como línea separada. |

---

## 7. Desglose Voyager - Videojuegos, mesa, gastronomía y contenido

| Desarrollo | Docs `.md` | Qué tiene | Valor | Acción |
|---|---:|---|---|---|
| **Dragón Alebrije** | 20 | Juego de cartas, 169 cartas, nahuales, faroleo, app digital, PRD. | Producto físico-digital más claro; IP mexicana. | Ejecutar versión digital primero. |
| **Coraline / Pink Palace** | 20 | Investigación visual, assets, GDD, modelos 3D. | Portafolio AAA, no monetizable por IP de terceros. | Pausar como portafolio. |
| **Kaetso** | 22 | RPG/narrativa, cosmogonía, personajes, casas, mecánicas, estética. | IP propia de videojuego/lore. | Congelar hasta tener publisher/recursos. |
| **Neko Nesushi** | 13 | Puzzle/casual japonés-felino. | IP ligera, posible mobile/casual. | Congelar. |
| **Die Rabbits Die** | 13 | Acción/dark humor. | Concepto. | Congelar. |
| **Hot Dog Hero** | 14 | Arcade/cocina/NYC. | Concepto comercial ligero. | Congelar. |
| **La Chica y el Zorro** | 14 | Narrativo/místico/futurista. | IP visual/narrativa. | Congelar. |
| **Nanny Ninja** | 13 | Sigilo/cuidado. | Concepto jugable. | Congelar. |
| **Viajeros** | 13 | Exploración procedural/multiverso. | Ambición alta. | Congelar. |
| **Casino AI Studio** | 4 | PRD, frontend, backend y protocolo de AI studio/casino. | Requiere revisión legal. | Revisar antes de mover. |
| **The Good Liar** | 13 | Deducción social/engaño. | Juego de mesa conceptual. | Congelar. |
| **Titanes** | 14 | Estrategia/mitología. | IP conceptual. | Congelar. |
| **Lotto di Pasta** | 13 | FoodTech, pasta paramétrica/3D, alta cocina. | Concepto B2B creativo. | Pausar como IP gastronómica. |
| **Música Daniel** | 12 | Composiciones, audios, canciones, material sonoro. | Activo de marca/contenido. | Archivo creativo. |
| **Closet a la Pantalla** | 13 | Ebook/fashion/digital. | Contenido editorial. | Congelar. |

---

## 8. Sociedad Unova y roles detectados

La documentación de `sociedad unova` rectifica el valor del ecosistema bajo tres perfiles:

| Perfil | Rol corregido | Pregunta que responde |
|---|---|---|
| **Daniel** | CPO/CIO: innovación, producto, IP, UX, IA, narrativa, prototipado. | ¿Qué idea vale la pena convertir en producto? |
| **Oliver** | CTO/CPE: factibilidad, ROI, arquitectura, rentabilidad y escalamiento. | ¿Esto se puede construir, sostener y monetizar? |
| **David** | CCO evolutivo: venta, validación, objeciones, cierre y voz del cliente. | ¿El cliente lo entiende, lo desea y lo compra? |

Implicación:

> Daniel no debe presentarse solo como diseñador o programador. La evidencia documental muestra que su valor central es originar IP, producto, experiencia y dirección de innovación.

---

## 9. Reacomodo recomendado de datos

### 9.1 `00_Gobernanza_y_Sociedad`

Debe contener:

- Sociedad Unova.
- Roles Daniel/Oliver/David.
- Pacto de socios.
- Protocolos de comunicación.
- Criterios de inversión.
- Documentos de financiamiento Rodrigo/Eduardo.

Rutas fuente:

- `sociedad unova`
- `plan de financiamiento`
- `desarrollo web unova games studio\unovagames_dossier`

### 9.2 `01_Productos_Financiables`

Debe contener solo productos con ruta comercial cercana.

| Producto | Motivo |
|---|---|
| Proyectia / TSK | Prioridad alta; productividad y gestión. |
| Switch Click Swiss | Utilidad clara para Windows/power users. |
| Dragón Alebrije digital | IP fuerte y producto diferenciable. |
| Julia AI / RAG local | Producto B2B para salud/legal/conocimiento privado. |
| Proyectia Tabs | Extensión barata de publicar y validar. |
| App Vivo | Prueba de entrega móvil comercial. |

### 9.3 `02_Activos_Tecnicos_Base`

Estos no siempre se venden solos, pero aceleran productos:

| Activo | Uso |
|---|---|
| ReactBite | Runtime/micro-app packaging. |
| Ethyria | Voz, IA local, interacción emocional. |
| Nodia | Agentes y automatización. |
| Asteria | IA visual local. |
| Voyager Files | Exploración/gestión de archivos. |
| MySoul | Lenguaje visual e identidad. |

### 9.4 `03_Portafolio_IP_Creativo`

Debe contener IP, mundos y demos visuales:

- Kaetso.
- Coraline como portafolio no monetizable.
- Neko Nesushi.
- Viajeros.
- La Chica y el Zorro.
- Lotto di Pasta.
- Música Daniel.
- Closet a la Pantalla.

### 9.5 `04_Backlog_Ordenado`

Debe contener ideas que no se desarrollan ahora:

- Debatia.
- MaterialCode.
- PredictIA.
- Quick Look.
- ComedyClick.
- WitchTricIA.
- MedicIA.
- VitalIA.
- Prompt-IA.
- iPad Magic Pro.
- UI Lab.

### 9.6 `05_Archivo_Historico_y_Evidencia`

Debe contener:

- `Retriver` y bóvedas de chats/documentos.
- `todos documentos`.
- Copias viejas de Ethyria/Nodia/Proyectia.
- Backups de Asteria/transparentimagen.
- CVs y portafolio personal.

Regla:

> El archivo histórico se consulta, pero no debe convertirse en workspace activo ni mezclarse con productos vivos.

---

## 10. Matriz de decisión inmediata

| Prioridad | Desarrollo | Decisión | Por qué |
|---:|---|---|---|
| 1 | Julia AI / RAG local | Ejecutar piloto B2B | Encaja con Rodrigo/Eduardo, privacidad y documentos. |
| 2 | Proyectia / TSK | Consolidar producto | Alta prioridad documental y comercial. |
| 3 | Switch Click Swiss | Preparar distribución | Utilidad clara, necesita QA/firma. |
| 4 | Dragón Alebrije digital | Preparar vertical IP | IP mexicana fuerte, mejor empezar digital. |
| 5 | ReactBite | Mantener base técnica | Empaqueta soluciones, no distraer como producto principal. |
| 6 | App Vivo | Usar como evidencia | Muestra entrega móvil comercial real. |
| 7 | Nodia/Ethyria | Preparar como módulos | Potentes, pero scope grande. |
| 8 | Asteria/VisualIA | Mantener aislado | IA visual, no mezclar con RAG. |
| 9 | Videojuegos AAA | Portafolio | Alta producción, no primera inversión. |
| 10 | Backlog apps | Congelar | Evitar dispersión. |

---

## 11. Próximo paso recomendado

Crear tres documentos derivados:

| Documento | Objetivo |
|---|---|
| `INVENTARIO_REACOMODADO_UNOVA_VOYAGER_2026.md` | Tabla formal final con cada proyecto y carpeta destino. |
| `PITCH_PRODUCTOS_FINANCIABLES_TOP_5.md` | Documento corto para inversores con Julia, Proyectia, SCS, Dragón Alebrije y Proyectia Tabs. |
| `PLAN_LIMPIEZA_CARPETAS_CANONICAS.md` | Plan para mover/copiar solo cuando el usuario autorice, sin borrar nada aún. |

No recomiendo mover carpetas todavía. Primero debe aprobarse la estructura de reacomodo para evitar perder contexto o mezclar archivos vivos con archivo histórico.

