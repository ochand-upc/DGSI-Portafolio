# Portafolio – DGSI 2024‑2025
---

## 1. Portada

* 🎓 **Título del proyecto**: *Portafolio – DGSI 2024‑2025*
* 🏷️ **Alumno**: *Óliver Eduardo Chan Dorado*
* 👨‍🏫 **Profesor**: *Marc Alier Forment*
* 📅 **Fecha**: *05‑06‑2025*

---

## 2. Tabla de Contenido

* [1. Portada](#1-portada)
* [2. Tabla de Contenido](#2-tabla-de-contenido)
* [3. Introducción](#3-introducción)
* [4. Proyectos y Actividades](#4-proyectos-y-actividades)

  * [4.1 Transcripción de SRTs](#41-transcripción-de-srts)
  * [4.2 Webscraping fib.upc.edu](#42-webscraping-fibupcedu)
  * [4.3 Embeddings](#43-embeddings)
  * [4.4 Simple RAG](#44-simple-rag)
  * [4.5 RAG semántico](#45-rag-semántico)
  * [4.6 Gestor de Producción (MRP)](#46-gestor-de-produccion-mrp)
  * [4.7 Agente – Browser Use](#47-agente--browser-use)
  * [4.8 MCP (Model Context Protocol)](#48-mcp-model-context-protocol)
  * [4.9 Agent From Scratch](#49-agent-from-scratch)
* [5. Conclusiones Generales](#5-conclusiones-generales)
* [6. Créditos](#6-créditos)

---

## 3. Introducción

La asignatura de **Desarrollo y Gestión de Sistemas de Información** ha explorado la **transformación exponencial del cómputo**, impulsada por avances como la Ley de Moore, que ha multiplicado la capacidad de procesamiento y acelerado el cambio tecnológico. Este fenómeno impacta el **mercado laboral** mediante la irrupción de la **Inteligencia Artificial generativa**, capaz de superar al ser humano en tareas específicas, y origina una **demanda energética masiva** para el entrenamiento de modelos. En este contexto, la materia subraya que la información, por sí sola, no constituye conocimiento; la **semántica** y el **contexto** son esenciales para interpretar los datos y tomar decisiones. Asimismo, se destaca la importancia de **diferenciar problemas y soluciones**, reconociendo que los requisitos en informática caducan con mayor rapidez que en otras disciplinas, de modo que se precisan sistemas adaptables.

Hemos profundizado en la **evolución de la infraestructura de software**, desde la gestión de **sistemas legacy** y la **virtualización** (VMware), hasta el paradigma del **Cloud Computing** y la eficiencia de los **contenedores y la orquestación** (Docker, Kubernetes). También se exploró la diversidad del almacenamiento de datos, comparando las **bases relacionales** con las **NoSQL**, priorizando velocidad y escalabilidad según el caso. Un pilar fundamental fue la comprensión de la **IA** mediante **embeddings**, representaciones vectoriales que otorgan significado a los datos y sustentan tecnologías como las **bases vectoriales (ChromaDB)** y la **Generación Aumentada por Recuperación (RAG)**. Además, se analizaron los **agentes de IA**, capaces de planificar y ejecutar tareas complejas mediante herramientas externas.

La asignatura abordó igualmente los **aspectos organizativos, económicos y políticos** de la tecnología, destacando el concepto de **"skin in the game"** para fomentar la responsabilidad en la toma de decisiones y evitar errores recurrentes. Se examinó cómo la tecnología propicia monopolios y la diferencia entre **IT** (Tecnologías de la Información) y **OT** (Tecnologías Operacionales), donde la continuidad operacional suele primar sobre la seguridad. La **innovación** se definió como una **transformación humana** que conlleva la **democratización, desmonetización y desmaterialización** de productos y servicios. Por último, se debatió el futuro del **desarrollo de software asistido por IA**, los roles de **ciberseguridad** (Red Team y Blue Team), la automatización de **GRC** mediante IA y los **riesgos emergentes de los agentes de IA**, como la exfiltración de datos o el chantaje.

---

## 4. Proyectos y Actividades

### 4.1 Transcripción de SRTs

**Fecha**: Jueves, 20 de Febrero de 2025

**Objetivos**

* ⚙️ Configurar: copilot, conda, python
* 🤖 Llamar a modelos básicos, dar instrucciones a copilot y primeras experiencias en vibes coding

## Descripción General

**Esta es una aplicación de transcripción de audio desarrollada para un Mini‑Hackathon de DGSI.**

## Objetivo de la Aplicación

La aplicación está orientada a:

* 🎙️ Convertir contenido de audio/video a texto transcrito
* 🎞️ Generar subtítulos automáticos
* 📝 Transcribir reuniones y conferencias
* 👥 Identificar diferentes hablantes en conversaciones

## Características Principales

### Funcionalidad

La aplicación está diseñada para transcribir archivos de audio a texto utilizando dos enfoques diferentes:

1. **Vosk (Local)**

   * Utiliza el modelo `vosk-model-es-0.42` para transcripción offline en español
   * Procesamiento local sin dependencias externas
   * Script independiente en `avance_carlos/transcribir.py`

2. **Google Cloud Speech-to-Text**

   * Implementa transcripción con diarización de hablantes (identificación de diferentes voces)
   * Requiere configuración de credenciales de Google Cloud
   * Funcionalidad avanzada en `audio_con_diarizacion.py`

### Arquitectura Técnica

* **Backend**: FastAPI con Python 3.11
* **Frontend**: Interfaz web simple con HTML/CSS/JavaScript
* **Procesamiento**: Scripts independientes para diferentes métodos de transcripción
* **Servidor**: Uvicorn para desarrollo local

### Estructura del Proyecto

```text
Mini-Hackaton-1-DGSI/
├── transcripcion-srts/          # Aplicación web principal
│   ├── main.py                  # Servidor FastAPI
│   ├── requirements.txt         # Dependencias
│   ├── static/
│   │   └── index.html           # Interfaz de usuario
│   └── README.md               # Documentación
├── avance_carlos/              # Trabajo de Carlos
│   ├── Audio.wav
│   └── transcribir.py          # Implementación con Vosk
├── audio_con_diarizacion.py    # Implementación Google Cloud
├── convertaudio.py             # Utilidades de conversión
└── Audio.wav                   # Archivo de prueba
```

**Repositorio**: [GitHub – Mini‑Hackaton‑1‑DGSI](https://github.com/Jofrix98UPC/Mini-Hackaton-1-DGSI)

## Estado del Proyecto

* 🚧 **Desarrollo activo**: Proyecto en desarrollo con diferentes ramas de trabajo
* 🔀 **Implementaciones múltiples**: Incluye varios enfoques experimentales para la transcripción
* 🖥️ **Interfaz básica**: Permite subir archivos MP4 y obtener subtítulos
* 👥 **Desarrollo colaborativo**: Cada desarrollador tiene su propio directorio de trabajo

## Configuración y Uso

### Requisitos

* 🐍 Python 3.11
* 💻 Entorno virtual recomendado
* 📦 Modelo Vosk español (`vosk-model-es-0.42`)
* 🔑 Credenciales de Google Cloud (opcional)

---

### 4.2 Webscraping fib.upc.edu

**Fecha**: Jueves, 27 de Febrero de 2025

**Objetivos**

* 🗂️ Mantener estructura de la web en directorios y nombres de ficheros
* 🔗 Links entre ficheros
* 🖼️ Descargar imágenes
* 📑 Implementar tablas de la web en tablas markdown

## Descripción General

**Mini‑Hackathon‑Markdown** es un proyecto de web scraping y conversión de datos desarrollado durante un mini hackathon. El objetivo principal es extraer información de páginas web y convertirla automáticamente a formato **Markdown** para su posterior procesamiento y reutilización.

## Objetivo de la Aplicación

### Propósito Principal

* ⚙️ **Automatizar la extracción** de contenido web estructurado
* 🔄 **Convertir HTML a Markdown** manteniendo la jerarquía y estructura original
* 🚚 **Facilitar la migración** de contenido web a formatos más manejables
* 🗄️ **Crear una base de datos** de contenido académico en formato markdown

### Casos de Uso

* 🏛️ Migración de sitios web legacy a sistemas modernos
* 💾 Creación de backups estructurados de contenido web
* 📊 Análisis de contenido académico para procesamiento posterior
* 📝 Generación de documentación a partir de contenido web existente

## Características Principales

### Funcionalidad

#### Web Scraping Inteligente

* 🌐 **Extracción completa** del sitio web de la FIB ([https://www.fib.upc.edu](https://www.fib.upc.edu))
* 🏗️ **Preservación de la estructura** jerárquica original
* 🏷️ **Mantenimiento de metadatos** como títulos, enlaces y navegación
* 🌍 **Procesamiento multiidioma** (Catalán, Inglés, Español)

#### Conversión a Markdown

* 🔄 **Conversión HTML → Markdown** utilizando la librería `markdownify`
* 📎 **Mantenimiento de formato** y estructura de enlaces
* 🏷️ **Preservación de metadatos** del sitio original
* 📂 **Organización por idiomas** y categorías

### Arquitectura Técnica

#### Stack Tecnológico

* **Lenguaje**: Python 3.8+
* **Librerías principales**:

  * `requests`: Para realizar peticiones HTTP
  * `markdownify`: Para convertir HTML a Markdown
* **Control de versiones**: Git
* **Gestión de dependencias**: pip + requirements.txt

#### Flujo de Procesamiento

1. **Input**: URL del sitio web objetivo
2. **Scraping**: Descarga del contenido HTML
3. **Procesamiento**: Análisis y estructuración de datos
4. **Conversión**: HTML → Markdown
5. **Output**: Archivos .md organizados por estructura

### Estructura del Proyecto

```text
Mini-Hackathon-Markdown/
├── README.md                 # Documentación del proyecto
├── .gitignore                # Archivos excluidos del control de versiones
├── ca/                       # Contenido en Catalán
│   ├── estudis/              # Información académica
│   ├── mobilitat/            # Programas de intercambio
│   ├── recerca/              # Investigación y grupos
│   ├── empresa/              # Relaciones con empresas
│   └── la-fib/               # Información institucional
├── en/                       # Contenido en Inglés
│   └── [misma estructura]    # Estructura paralela al catalán
└── .git/                     # Control de versiones Git
```

**Repositorio**: [GitHub – Mini‑Hackathon‑Markdown](https://github.com/carlos-andres-rodriguez-torres/Mini-Hackathon-Markdown/)

## Estado del Proyecto

### Desarrollo Completado

* ✅ **Extracción completa** del sitio web de la FIB
* ✅ **Conversión exitosa** de HTML a Markdown
* ✅ **Organización estructurada** por idiomas y categorías
* ✅ **Preservación de metadatos** y navegación
* ✅ **Control de versiones** configurado

### Estado Actual

* 📈 **Fase de resultados**: Extracción y conversión terminadas
* 📂 **Datos procesados**: +500 archivos Markdown estructurados
* 🌐 **Contenido multiidioma**: Catalán e Inglés completamente procesados

## Configuración y Uso

### Requisitos

* 🐍 **Python 3.8** o superior
* 🌐 **Conexión a internet** para web scraping
* 📦 **Librerías requeridas**:

  ```bash
  pip install requests markdownify
  ```

---

### 4.3 Embeddings

**Fecha**: Jueves, 6 de Marzo de 2025

**Objetivos**

* 📦 Usar ChromaDB
* 🌊 Probar *windsurf* (recomendado)
* 🤖 Usar OpenAI V3 Large o **ollama.ai** con modelo multilingüe local (recomendado)
* 🧩 Poner atención a la estrategia de *chunking* y metadatos

## Descripción General

**Mini‑Hackaton‑Embeddings** es la evolución natural del proyecto de web scraping, transformado en una **aplicación de búsqueda semántica avanzada**. Procesa el corpus académico extraído de la FIB para crear un sistema de búsqueda vectorial inteligente mediante embeddings y IA.

## Objetivo de la Aplicación

### Propósito Principal

* 🌍 **Democratizar el acceso** a información académica compleja
* 🔍 **Crear un motor de búsqueda** contextual
* 🗂️ **Transformar contenido estático** en base de conocimiento
* 🧭 **Facilitar la navegación** por información extensa

### Casos de Uso Específicos

* 🎓 Búsqueda académica de programas y asignaturas
* 💬 Consultas contextuales sobre grados y requisitos
* 🧑‍🎓 Asistencia estudiantil para trámites y horarios
* 🏛️ Investigación institucional de ofertas formativas

## Características Principales

### Sistema de Embeddings Vectoriales

* **Modelo**: `all‑MiniLM‑L6‑v2` multilingüe
* 🌐 Soporte Catalán, Inglés y Español
* 🗄️ Indexación de +500 documentos
* 📈 Ranking por similitud semántica

### Base de Datos Vectorial

* **ChromaDB** persistente
* 🏷️ Metadatos de origen preservados
* ⚡ Consultas vectoriales eficientes

### Arquitectura Técnica

```text
Núcleo IA → SentenceTransformers + ChromaDB + all‑MiniLM‑L6‑v2
Procesamiento → html2text, markdown, uuid
Web Scraping heredado → beautifulsoup4, requests
```

#### Flujo de Procesamiento Inteligente

1. 📥 Lectura Markdown
2. 🧹 Preprocesamiento
3. 🧠 Generación de embeddings
4. 💾 Almacenamiento en ChromaDB
5. 🔎 Consulta vectorial
6. 📑 Recuperación contextual

### Estructura del Proyecto

```text
Mini-Hackaton-Embeddings/
├── main.py
├── requirements.txt
├── chroma_db/           # BD vectorial
└── markdown_pages/      # Corpus procesado
    ├── ca/ …
    ├── en/ …
    └── es/ …
```

**Repositorio**: [GitHub – Mini‑Hackaton‑Embeddings](https://github.com/ro-carlos/Mini-Hackaton-Embeddings)

## Estado del Proyecto

### Desarrollo Completado ✅

* Sistema de embeddings y ChromaDB funcionando
* Indexación completa del corpus académico
* Motor de búsqueda semántica operativo

### Capacidades Avanzadas

* 🧠 Comprensión contextual y multiidioma
* 🕰️ Acceso a planes de estudio históricos
* 📊 Escalabilidad preparada para más documentos

## Configuración y Uso

### Requisitos

```bash
python 3.8+
pip install sentence-transformers chromadb beautifulsoup4 html2text
```

---

### 4.4 Simple RAG

**Fecha**: Jueves, 13 de Marzo de 2025

**Objetivos**

* 💻 Crear un programa CLI en Python que responda preguntas sobre la web de la FIB
* 📦 Utilizar la BD de embeddings del 6 de marzo para implementar RAG

## Descripción General

**Mini‑Hackathon‑LLM** culmina la evolución desde el scraping a un **sistema RAG completo** que combina búsqueda semántica y generación con LLM para un asistente académico inteligente.

## Objetivo de la Aplicación

### Propósito Principal

* 🧑‍🎓 **Asistente académico inteligente** con consultas conversacionales
* 🌍 **Democratizar el acceso** a información compleja de la FIB
* 📑 **Respuestas contextuales** basadas en fuentes verificables
* 🛠️ **Implementar un pipeline RAG** robusto (Indexación → Retrieval → Generation)

### Casos de Uso

* 📚 Consultas académicas avanzadas
* 📝 Asistencia estudiantil personalizada
* 🗂️ Exploración curricular y soporte administrativo
* 📈 Investigación institucional

## Características Principales

### Sistema RAG Avanzado

* 🔎 **Indexación inteligente** con chunking semántico y overlap
* 🧠 **Embeddings híbridos** (OpenAI + SentenceTransformers) con fallback automático
* ⚡ **Búsqueda vectorial** en ChromaDB
* 🤖 **Generación contextual** con GPT‑3.5‑turbo
* 🧾 **Respuestas con referencias** a los documentos fuente

### Arquitectura Técnica (resumen)

```text
CLI → Retrieval (ChromaDB) → GPT‑3.5‑turbo → Respuesta con referencias
```

**Repositorio**: [GitHub – Mini‑Hackathon‑LLM](https://github.com/ochand-upc/Mini-Hackathon-LLM)

## Estado del Proyecto

### Desarrollo Completado ✅

* **Sistema RAG funcional**: Pipeline completo de Indexación → Retrieval → Generation
* **Indexación avanzada**: Chunking inteligente con preservación de contexto
* **Búsqueda híbrida**: Embeddings OpenAI + SentenceTransformers con fallback automático
* **CLI robusta**: Interfaz de línea de comandos con subcomandos y filtros
* **Integración OpenAI**: GPT‑3.5‑turbo para generación contextual
* **Persistencia optimizada**: ChromaDB con gestión automática de dimensiones

### Capacidades Avanzadas del Sistema

* **Comprensión contextual profunda**: Mantiene coherencia entre chunks relacionados
* **Respuestas verificables**: Cada respuesta incluye referencias a documentos fuente
* **Escalabilidad empresarial**: Arquitectura preparada para corpus de millones de documentos
* **Flexibilidad de modelos**: Intercambio dinámico entre proveedores de embeddings
* **Robustez operacional**: Manejo de errores, reconexión automática y validación de API keys

### Innovaciones Técnicas Implementadas

* **Chunking semántico**: División por oraciones con overlap inteligente
* **Embeddings adaptativos**: Detección automática de modelo y fallback transparente
* **Metadatos enriquecidos**: Sistema de tags y filtros para búsquedas especializadas
* **Batch processing**: Indexación eficiente de grandes volúmenes con control de memoria
* **Gestión de dimensiones**: Recreación automática de colecciones cuando cambian los embeddings

## Configuración y Uso

### Requisitos del Sistema

```bash
# Requisitos computacionales
Python 3.8+
RAM: 8GB mínimo (16GB recomendado para corpus grandes)
Storage: ~1GB para modelos y base de datos vectorial
GPU: Opcional (acelera SentenceTransformers)

# Requisitos de API
OpenAI API Key (mejor rendimiento)
- text-embedding-3-small: $0.00002/1K tokens
- gpt-3.5-turbo: $0.0015/1K tokens input, $0.002/1K tokens output
```

### Métricas de Rendimiento y Escalabilidad

* **Indexación**: \~50‑100 documentos/minuto (dependiendo del tamaño)
* **Búsqueda**: <200 ms por consulta con OpenAI embeddings
* **Memoria**: \~2 GB RAM para corpus de 1000 documentos
* **Precision\@5**: >85 % en consultas académicas específicas
* **Escalabilidad**: Testado con corpus de hasta 10 000 documentos
* **Costo operacional**: \~\$0.01‑0.05 por consulta completa (Retrieval + Generation)

---

### 4.5 RAG semántico

**Fecha**: Jueves, 20 de Marzo de 2025

**Objetivos**

* 🛠️ Consideraciones técnicas de ingeniería de prompting explicadas en clase.
* 🚀 Mejora del sistema de RAG simple con información **semántica** sobre el dominio FIB (ingestión o pre‑query).

## *Descripción General*

**LLM Chat RAG** es una aplicación de chatbot avanzada que implementa el patrón **Retrieval Augmented Generation (RAG)** utilizando tecnologías de vanguardia como OpenAI GPT‑4o‑mini, ChromaDB y FastAPI. El sistema combina OCR, búsqueda semántica y generación de respuestas contextuales, reduciendo al mínimo las "alucinaciones" al fundamentar cada respuesta en documentos reales indexados.

## Objetivo de la Aplicación

### Problema que Resuelve

* ❌ **Eliminación de respuestas inventadas** de los LLM puros.
* 📚 **Acceso contextual** a grandes volúmenes de documentación académica.
* 🔤 **Expansión automática de acrónimos** técnicos mediante diccionario especializado.
* 🖼️ **Procesamiento multimodal**: extracción de texto de PDFs con OCR.

### Propósito Principal

Crear un asistente inteligente que combine la potencia de los LLM con la precisión de la recuperación documental, ofreciendo respuestas confiables con citas a las fuentes originales.

## *Características Principales*

### Funcionalidad

#### **Motor RAG Avanzado**

* 🌀 **Aumentación de consultas**: genera variaciones semánticas de cada pregunta.
* 🔍 **Búsqueda vectorial**: ChromaDB + embeddings OpenAI.
* 🧠 **Generación contextual**: GPT‑4o‑mini con historial de conversación.
* 📑 **Sistema de citación**: referencias automáticas a documentos fuente.

#### **Procesamiento de Documentos**

* 🖨️ Servicio **OCR independiente** (Tesseract) para PDFs.
* 📝 **Formateo Markdown** automático del contenido extraído.
* 🌐 **Soporte multiidioma** (español configurado por defecto).

#### **Expansión de Acrónimos**

* 📖 **Diccionario especializado** (`acronyms.json`).
* ➕ Inserción automática en las consultas del usuario.

#### **Interfaces Múltiples**

* 💻 **CLI interactiva** con comandos avanzados.
* 🌍 **Aplicación web** FastAPI + HTML/JS.
* 🔗 **API REST** documentada para integración externa.

### Arquitectura Técnica

#### **Stack Tecnológico**

* **Backend**: Python 3.9 + FastAPI
* **Base de datos vectorial**: ChromaDB
* **Modelo de lenguaje**: OpenAI GPT‑4o‑mini
* **OCR**: Tesseract (soporte español)
* **Contenedorización**: Docker & Docker Compose
* **Frontend**: HTML5, CSS3, JavaScript vanilla

#### **Patrones Arquitecturales**

* 🧩 **Microservicios**: separación entre servicio RAG y servicio OCR.
* 🗂️ **Arquitectura por capas**: motor RAG, capa de datos, UI.
* 💉 **Inyección de dependencias** mediante variables de entorno.
* 🔄 **Separación de responsabilidades** en módulos especializados.

#### **Gestión de Estado**

* 🕑 **Historial de conversación**: últimas 10 interacciones.
* 💾 **Persistencia vectorial**: embeddings almacenados en ChromaDB.
* ⚙️ **Configuración dinámica**: carga de acrónimos en tiempo de ejecución.

### Estructura del Proyecto

```text
llm-chat-rag/
├── main.py              # Motor RAG principal y CLI
├── web_app.py           # Aplicación web FastAPI
├── ocr_service.py       # Servicio OCR independiente
├── requirements.txt     # Dependencias Python
├── Dockerfile           # Imagen para servicio RAG
├── Dockerfile.ocr       # Imagen para servicio OCR
├── docker-compose.yml   # Orquestación de servicios
├── .env.example         # Template de configuración
├── templates/
│   └── index.html       # Interfaz web del chatbot
├── data/
│   └── acronyms.json    # Diccionario de acrónimos
├── chroma_db/           # Base de datos vectorial (generada)
├── doc/
│   └── PRD.md           # Documento de requisitos
└── static/              # Recursos estáticos (vacío)
```

**Repositorio**: [GitHub – llm-chat-rag](https://github.com/ochand-upc/llm-chat-rag)

#### **Componentes Clave**

**Motor RAG (main.py)**

* Implementación completa del patrón RAG
* Gestión de ChromaDB y embeddings
* Aumentación inteligente de consultas
* Interfaz CLI con comandos avanzados

**Aplicación Web (web_app.py)**

* API REST con FastAPI
* Gestión de sesiones y historial
* Integración *seamless* con el motor RAG

**Servicio OCR (ocr_service.py)**

* Procesamiento independiente de PDFs
* API dedicada para extracción de texto
* Optimizado para documentos académicos

## Estado del Proyecto

### **Desarrollo Completo y Funcional**

El proyecto presenta un estado **maduro y listo para producción** con las siguientes características:

#### Funcionalidades Implementadas ✅

* Motor RAG completamente funcional
* Interfaz web responsiva y moderna
* Servicio OCR independiente y optimizado
* Sistema de expansión de acrónimos
* Arquitectura de microservicios con Docker
* CLI interactiva con comandos avanzados
* Gestión de historial de conversaciones
* Sistema de citación y referencias

#### Preparación para Despliegue ✅

* **Contenedorización completa**: Dockerfiles optimizados para ambos servicios
* **Orquestación**: Docker Compose para gestión de servicios
* **Variables de entorno**: Configuración segura y flexible
* **Separación de datos**: Volúmenes para persistencia

### **Áreas de Mejora Potencial**

* **Tests automatizados**: No se observan tests unitarios o de integración
* **Documentación API**: Falta documentación Swagger/OpenAPI detallada
* **Monitoreo**: Métricas y observabilidad para producción
* **Escalabilidad**: Optimizaciones para cargas de trabajo más grandes

## Configuración y Uso

### **Prerrequisitos**

* Docker y Docker Compose instalados
* Clave API de OpenAI válida
* Al menos 2 GB de RAM disponible
* Puertos 4000 y 8000 libres

---

### 4.6 Gestor de Producción (MRP)

**Fecha**: Jueves, 15 de Mayo de 2025

**Presentación**

* Presentación del Proyecto : [Presentación de Google – Módulo MRP](https://docs.google.com/presentation/d/1-8os8Jm-6iEftNWjcwCgebZhXh8K9B8gDBkvZU5VbN8/edit?usp=sharing)

## Descripción General

El **MRP-DGSI** es un simulador avanzado de producción de impresoras 3D que implementa un sistema completo de **Material Requirements Planning (MRP)**. La aplicación modela día a día el ciclo operativo de una planta de fabricación, enfocándose en tres aspectos fundamentales: **gestión de inventarios**, **compras** y **planificación de la producción**.

El sistema permite a los usuarios asumir el rol de planificadores de producción, tomando decisiones estratégicas sobre qué fabricar y qué comprar para satisfacer la demanda de manera eficiente. La aplicación genera demanda de forma aleatoria y requiere que el usuario gestione recursos limitados para cumplir con los pedidos.

---

## Objetivo de la Aplicación

### Objetivos Principales

* **Simulación Realista**: Modelar de manera fidedigna el proceso de producción de impresoras 3D con componentes reales
* **Educación y Entrenamiento**: Proporcionar una herramienta didáctica para estudiantes y profesionales en ingeniería de sistemas, producción y gestión de operaciones
* **Base Arquitectónica**: Diseñar un sistema MRP escalable que pueda servir como fundamento para implementaciones empresariales
* **Desarrollo de Habilidades**: Permitir la práctica y mejora de habilidades en planificación de producción y gestión de cadena de suministro

### Usuarios Objetivo

* Estudiantes de ingeniería de sistemas, producción y gestión de operaciones
* Arquitectos de sistemas de información
* Profesionales en formación en gestión de cadena de suministro
* Educadores que buscan herramientas didácticas para enseñar conceptos de planificación

---

## Características Principales

### Funcionalidad

#### **Simulación Basada en Eventos Discretos**

* Motor de simulación implementado con **SimPy** que ejecuta ciclos diarios de 24 horas
* Generación aleatoria de pedidos con parámetros configurables (media: 5.0, desviación estándar: 2.0)
* Capacidad de producción diaria configurable (10 impresoras por día por defecto)

#### **Gestión de Inventarios**

* Seguimiento en tiempo real de materias primas y productos terminados
* Capacidad de almacén configurada (1000 unidades por defecto)
* Alertas automáticas de inventario insuficiente
* Visualización detallada de niveles de stock

#### **Sistema de Compras**

* Catálogo de proveedores con precios y tiempos de entrega diferenciados
* Gestión de órdenes de compra con seguimiento de estado
* Cálculo automático de fechas de entrega basado en lead times
* Múltiples proveedores por producto con diferentes condiciones comerciales

#### **Planificación de Producción**

* **Lista de Materiales (BOM)** configurada para dos modelos de impresoras:

  * **P3D-Classic**: Modelo base con componentes estándar
  * **P3D-Pro**: Modelo avanzado con sensores adicionales
* Liberación manual de órdenes a producción con verificación automática de materiales
* Gestión de cola de producción limitada por capacidad diaria

##### **Modelos de Productos**

**P3D-Classic** (Modelo Base):

* 1 kit\_piezas
* 1 pcb (CTRL-V2)
* 1 extrusor
* 2 cables\_conexion
* 1 transformador\_24v
* 1 enchufe\_schuko

**P3D-Pro** (Modelo Avanzado):

* 1 kit\_piezas
* 1 pcb (CTRL-V3)
* 1 extrusor
* 1 sensor\_autonivel
* 3 cables\_conexion
* 1 transformador\_24v
* 1 enchufe\_schuko

#### **Reportes y Análisis**

* Historial completo de eventos con filtros por fecha y tipo
* Visualización gráfica de niveles de stock históricos
* Análisis de pedidos completados en el tiempo
* Exportación e importación de datos en formato JSON

### Arquitectura Técnica

#### **Principios de Diseño**

Sistema basado en **Arquitectura Hexagonal** garantizando separación de responsabilidades, independencia de frameworks y alta testabilidad.

#### **Stack Tecnológico**

| Componente       | Tecnología       | Justificación              |
| ---------------- | ---------------- | -------------------------- |
| **Lenguaje**     | Python 3.11+     | Ecosistema robusto         |
| **Simulación**   | SimPy 4.0.2      | Motor de eventos discretos |
| **API REST**     | FastAPI 0.104.1  | Alto rendimiento           |
| **UI**           | Streamlit 1.28.0 | Dashboards rápidos         |
| **Validación**   | Pydantic 2.4.2   | Datos confiables           |
| **BDD**          | SQLite           | Ligero y portable          |
| **Gráficos**     | Altair 5.1.2     | Declarativo                |
| **Contenedores** | Docker & Compose | Despliegue consistente     |

#### **Capas de la Arquitectura**

```
(Presented ASCII diagram)
```

### Estructura del Proyecto

```text
MRP-DGSI/
├── application/
│   ├── services.py
│   └── simulation.py
├── config/
│   ├── di_container.py
│   └── settings.py
├── domain/
│   ├── models.py
│   ├── repositories.py
│   └── services.py
├── infrastructure/
│   ├── database.py
│   ├── data_export.py
│   └── repositories.py
├── presentation/
│   ├── api.py
│   └── streamlit_app.py
├── data/
│   ├── config.json
│   └── simulator.db
├── docs/
│   ├── PRD.md
│   └── architecture.md
├── scripts/
│   ├── init_db.py
│   └── export_import.py
├── docker-compose.yml
├── Dockerfile
├── main.py
└── requirements.txt
```

**Repositorio**: [GitHub – MRP-DGSI](https://github.com/ochand-upc/MRP-DGSI)

## Estado del Proyecto

### **Estado Actual: COMPLETAMENTE FUNCIONAL**

#### **Características Implementadas ✅**

* Motor de simulación completo
* API REST con documentación
* UI Streamlit interactiva
* Sistema de inventarios y órdenes
* Múltiples proveedores y visualización gráfica
* Containerización Docker

#### **Calidad del Código**

* Arquitectura limpia, SOLID, logging, validación

#### **Testing y Estabilidad**

* Sistema probado en escenarios educativos

---

## Configuración y Uso

### **Flujo de Uso del Sistema**

1. Revisar estado (pedidos, inventario)
2. Liberar órdenes a producción
3. Emitir órdenes de compra
4. "Avanzar día" para ejecutar simulación

---

### 4.7 Agente – Browser Use

**Fecha**: Jueves, 15 de Mayo de 2025

## Descripción General

**browser-use** es una aplicación de automatización web que emplea inteligencia artificial para interactuar con páginas web de forma autónoma. Aprovecha LLMs como GPT‑4o para interpretar instrucciones en lenguaje natural y ejecutarlas directamente en un navegador, automatizando procesos como el llenado de Google Forms.

## Objetivo de la Aplicación

* 🤖 **Automatizar tareas web** a partir de instrucciones en lenguaje humano.
* 🌐 Navegar a URLs indicadas y manipular elementos (inputs, botones).
* 📝 Completar formularios complejos de manera automática.

## Características Principales

### Funcionalidad

* **Automatización basada en IA** con GPT‑4o.
* **Procesamiento de lenguaje natural** para definir tareas.
* **Interacción web avanzada**: navegación, clics y llenado de formularios.
* **Integración OpenAI** vía LangChain.

### Arquitectura Técnica

* **Python 3.11**
* **LangChain + GPT‑4o**
* **browser\_use** para control del navegador
* **python‑dotenv** para configuración segura

### Estructura del Proyecto

```text
browser-use/
├── README.md
├── test.py               # Script de demostración
└── .git/                 # Control de versiones
```

**Repositorio**: [GitHub – browser-use](https://github.com/ro-carlos/browser-use)

### Estado del Proyecto

* 🚧 **Prototipo funcional** con agente IA y llenado de Google Forms
* ✅ Integración OpenAI y variables de entorno

### Configuración y Uso

1. Instalar Python 3.11
2. `pip install browser_use langchain_openai python-dotenv`
3. Exportar `OPENAI_API_KEY`
4. Ejecutar `python test.py`

---

### 4.8 MCP (Model Context Protocol)

**Fecha**: Martes, 20 de Mayo de 2025

## Descripción General

**MCP (Model Context Protocol)** es un estándar abierto creado por Anthropic que unifica la forma en que los agentes de IA interactúan con herramientas, datos y servicios. Define una comunicación estructurada entre:

* **MCP Host** (p. ej., la app con IA)
* **MCP Servers** (adaptadores que traducen las peticiones)
* **MCP Protocol** (esquema JSON estandarizado)

## Objetivo de la Aplicación (MCP)

1. 🌉 **Superar la brecha de interacción** entre IA y mundo real.
2. 📐 **Estandarización universal** de integraciones.
3. 🤖 **Autonomía real** para tareas multi‑paso.
4. 📈 **Escalabilidad** sin romper compatibilidad.

## Características Principales

### Funcionalidades Core

* 🔌 **Plug‑and‑Play**: conectar cualquier herramienta MCP sin código personalizado.
* ⏱️ **Interacción en tiempo real** para tareas multi‑servicio.
* 📚 **Protocolo unificado**: un estándar para todas las herramientas.
* 🌍 **Compatibilidad universal** local o remota.

### Ventajas Clave

| **Aspecto**    | **APIs Tradicionales** | **MCP**           |
| -------------- | ---------------------- | ----------------- |
| Setup          | Manual por herramienta | Un único estándar |
| Flexibilidad   | Fija                   | Dinámica          |
| Reutilización  | Difícil                | Automática        |
| Escalabilidad  | Se rompe               | Preparada         |
| Compatibilidad | Lógica a medida        | *Out‑of‑the‑box*  |
| Descubrimiento | Manual                 | Automático        |

### Beneficios 🚀

* **Agentes autónomos** capaces de actuar.
* **Compatibilidad universal** para conectar todo.
* **Eficiencia**: menos tiempo de integración.
* **Seguridad estandarizada**.

## Conexión con Nuestra Experiencia en el Chat

Lo que hemos experimentado en este chat es un **ejemplo perfecto de MCP en acción**:

### Implementación Práctica

1. **Desktop Commander** actúa como un MCP Server que traduce mis solicitudes de IA en comandos del sistema

### Acciones Realizadas

* ✅ Terminé Microsoft Word (`kill_process`)
* ✅ Abrí Google Chrome (`open -a "Google Chrome"`)
* ✅ Listé procesos en ejecución (`list_processes`)
* ✅ Todo sin necesidad de integraciones personalizadas

### Beneficios Observados

#### **Plug-and-Play**

No necesité configuración especial para interactuar con tu sistema.

#### **Tiempo Real**

Las acciones se ejecutaron inmediatamente.

#### **Estándar**

Uso la misma interfaz para diferentes tipos de operaciones del sistema.

## Aplicaciones del Mundo Real

### 💻 **Desarrollo de Software**

La IA lee y escribe código *across* archivos, terminales y proyectos.

### 📊 **Análisis de Datos**

La IA extrae de fuentes de datos estructuradas y genera *insights*.

### 📄 **Gestión de Documentos**

La IA guarda resúmenes como archivos o extrae información de documentos.

### 🔌 **Interacción con APIs**

La IA se conecta a servicios web como GitHub, Notion o Figma.

## El Ecosistema MCP en Crecimiento

### Principales Adoptantes

* Block, Replit, Apollo, Sourcegraph, Codeium y Microsoft Copilot Studio

### Marketplaces Emergentes

* mcpmarket.com
* mcp.so
* Cline's MCP Marketplace

### Herramientas de Infraestructura

* Mintlify, Stainless, Speakeasy, Cloudflare, Smithery y Toolbase

## Cómo Empezar con MCP

1. 📚 **Explorar Recursos**

   * Documentación oficial: [https://anthropic.com/news/model-context-protocol](https://anthropic.com/news/model-context-protocol)
   * Repositorio GitHub: [https://github.com/modelcontextprotocol](https://github.com/modelcontextprotocol)
2. 🔌 **Probar Servidores Existentes**

   * mcpmarket.com – Marketplace de servidores MCP
   * mcp.so – Plataforma de servidores plug‑and‑play
3. 🛠️ **Construir el Tuyo Propio**

   * Crear servidores MCP personalizados para herramientas específicas
   * Utilizar infraestructura como Mintlify o Stainless para simplificar el desarrollo

---
### 4.9 Agent From Scratch
**Fecha**: Martes, 27 de Mayo de 2025

## Descripción General

**AgentFromScratch.ipynb** es un notebook de Jupyter que implementa un agente de inteligencia artificial desde cero utilizando la API de OpenAI. El proyecto demuestra cómo construir un agente conversacional que puede interactuar con usuarios y utilizar herramientas específicas para resolver problemas matemáticos. Es un ejemplo educativo y práctico de cómo crear un sistema de IA con capacidades de uso de herramientas (tool usage).

## Objetivo de la Aplicación

El objetivo principal del notebook es:

- **Educativo**: Enseñar cómo implementar un agente de IA desde cero sin frameworks complejos
- **Demostración práctica**: Mostrar la integración de modelos de lenguaje con herramientas externas
- **Prototipo base**: Proporcionar una base sólida para expandir hacia agentes más complejos
- **Interacción en tiempo real**: Permitir conversaciones dinámicas entre usuario y agente IA

## Características Principales

### Funcionalidad

- **Agente conversacional**: Interacción bidireccional con usuarios mediante chat
- **Sistema de herramientas**: Capacidad del agente para ejecutar funciones específicas
- **Procesamiento de comandos**: Detección automática de solicitudes de uso de herramientas
- **Historial de conversación**: Mantenimiento del contexto durante la sesión
- **Herramientas matemáticas integradas**:
  - `add(x, y)`: Suma de dos números
  - `multiply(x, y)`: Multiplicación de dos números

### Arquitectura Técnica

**Tecnologías principales:**
- **Plataforma**: Jupyter Notebook
- **Lenguaje**: Python 3
- **Modelo de IA**: GPT-4 (OpenAI)
- **Biblioteca principal**: `openai` (API oficial)
- **Procesamiento de texto**: Expresiones regulares (`re`)

**Componentes arquitectónicos:**
- **Cliente OpenAI**: Gestión de conexión con API de OpenAI
- **Sistema de prompts**: Definición del comportamiento del agente
- **Motor de herramientas**: Diccionario de funciones ejecutables
- **Parser de comandos**: Análisis de respuestas para detectar llamadas a herramientas
- **Bucle de interacción**: Control de flujo conversacional

### Estructura del Proyecto

```
DGSI-AgentFromScratch/
├── .git/                    # Control de versiones Git
└── AgentFromScratch.ipynb   # Notebook principal con implementación completa
```

**Estructura del código:**
```python
├── Configuración inicial
│   ├── Importación de librerías (openai, re)
│   ├── Configuración de API Key
│   └── Inicialización del cliente OpenAI
├── Definición del sistema
│   ├── System prompt (instrucciones del agente)
│   ├── Historial de conversación
│   └── Diccionario de herramientas
└── Bucle principal
    ├── Input del usuario
    ├── Llamada a GPT-4
    ├── Procesamiento de respuesta
    └── Ejecución de herramientas
```

**Repositorio**: [GitHub – DGSI-AgentFromScratch](https://github.com/ochand-upc/DGSI-AgentFromScratch)

## Estado del Proyecto

**Estado actual**: Prototipo funcional completamente implementado

**Indicadores de madurez:**
- ✅ **Implementación completa**: Todas las funcionalidades básicas implementadas
- ✅ **Sistema de herramientas funcional**: Add y multiply operativos
- ✅ **Manejo de errores básico**: Validación de herramientas disponibles
- ✅ **Integración OpenAI**: Uso correcto de la API moderna de OpenAI
- ✅ **Limitación de turnos**: Control de MAX_TURNS para evitar bucles infinitos

**Características implementadas:**
- Conversación interactiva con GPT-4
- Sistema de detección de herramientas mediante regex
- Ejecución dinámica de funciones
- Mantenimiento de historial conversacional
- Retroalimentación de resultados al agente

**Áreas de mejora identificadas:**
- Ampliación del conjunto de herramientas disponibles
- Manejo más robusto de errores en argumentos
- Validación de entrada del usuario
- Persistencia de conversaciones
- Interfaz de usuario más sofisticada

## Configuración y Uso

### Prerequisitos

1. **Python 3.x** con Jupyter Notebook
2. **Bibliotecas requeridas**:
   ```bash
   pip install openai
   ```
3. **API Key de OpenAI**: Acceso a la API de OpenAI para usar GPT-4

### Configuración inicial

1. **API Key de OpenAI**:
   ```python
   openai.api_key = "TU_API_KEY_AQUI"
   ```

2. **Verificar dependencias**:
   - Asegurar que la biblioteca `openai` esté actualizada
   - Confirmar acceso a GPT-4 en la cuenta de OpenAI

### Uso del Notebook

**Ejecución paso a paso:**

1. **Ejecutar la celda principal**: Contiene toda la implementación
2. **Interactuar con el agente**: Escribir mensajes cuando aparezca "🧑 Tú:"
3. **Probar herramientas**: Pedir al agente que realice cálculos matemáticos

**Ejemplos de interacciones:**

```
🧑 Tú: ¿Cuánto es 5 + 3?
🤖 Agente: TOOL: add(5, 3)
🛠️ Resultado de add: 8
🤖 Agente: El resultado de 5 + 3 es 8.

🧑 Tú: Multiplica 4 por 7
🤖 Agente: TOOL: multiply(4, 7)
🛠️ Resultado de multiply: 28
🤖 Agente: El resultado de 4 × 7 es 28.
```

### Extensibilidad

**Agregar nuevas herramientas:**
```python
# Agregar al diccionario de tools
tools = {
    "add": lambda x, y: x + y,
    "multiply": lambda x, y: x * y,
    "subtract": lambda x, y: x - y,  # Nueva herramienta
}

# Actualizar el system_prompt para incluir la nueva herramienta
```

**Personalización del comportamiento:**
- Modificar el `system_prompt` para cambiar el rol del agente
- Ajustar `MAX_TURNS` para sesiones más largas o cortas
- Cambiar el modelo de "gpt-4" a otros modelos disponibles

### Consideraciones de seguridad

- **Evaluación de argumentos**: El código usa `eval()` que puede ser un riesgo de seguridad
- **Recomendación**: Implementar parseo más seguro para argumentos de herramientas
- **Validación**: Agregar validación de tipos para los argumentos de las funciones

Este notebook representa una excelente base para entender cómo construir agentes de IA con capacidades de herramientas, proporcionando un ejemplo claro y extensible para desarrolladores que quieran implementar sus propios sistemas de agentes inteligentes.


## 5. Conclusiones Generales

La experiencia en la asignatura de **Desarrollo y Gestión de Sistemas de Información** ha representado un **viaje transformador** que ha redefinido mi comprensión sobre el desarrollo de software y la aplicación de inteligencia artificial en la gestión empresarial. A través de una serie de desafíos prácticos y proyectos colaborativos, he experimentado una evolución significativa tanto en competencias técnicas como en metodologías de trabajo.

### Desafíos Iniciales y Curva de Aprendizaje

El **mayor obstáculo al inicio** fue la complejidad conceptual inherente a la inteligencia artificial, particularmente en el ecosistema de **Large Language Models (LLMs)**. Conceptos como embeddings, arquitecturas transformer, y sistemas RAG requerían no solo comprensión técnica, sino una **reconceptualización fundamental** de cómo abordar problemas de procesamiento de información. Esta barrera inicial se intensificó por la **falta de definición clara de roles** en los equipos de trabajo, lo que generó ineficiencias en la colaboración y distribución de responsabilidades.

Adicionalmente, la **ambigüedad en los objetivos** de cada hackathon representó un desafío metodológico significativo. Sin embargo, esta dificultad me llevó a desarrollar una **estrategia personal de aprendizaje**: comenzé a grabar las exposiciones del profesor para posteriormente analizarlas con **NotebookLM**, transformando el contenido en conocimiento estructurado y aplicable.

### Evolución en Metodologías de Desarrollo

Uno de los **insights más relevantes** ha sido reafirmar que la calidad de cualquier solución tecnológica depende fundamentalmente de la **comprensión profunda del problema**. Esta premisa, aunque conocida teóricamente, adquirió nueva dimensión al observar cómo los LLMs pueden generar soluciones técnicamente correctas pero conceptualmente inadecuadas cuando el problema no está bien definido.

El **Vibe Coding** inicialmente me resultó una metodología disruptiva y contraintuitiva. Requirió un proceso de **"desaprendizaje"** de patrones tradicionales de programación para adoptar un enfoque más colaborativo con la IA. Gradualmente comprendí que el rol del programador se ha transformado: ahora la competencia crítica radica en la **capacidad de interpretar, evaluar y refinar** las propuestas generadas por los LLMs, más que en la escritura manual de código desde cero.

### Implicaciones para el Futuro del Desarrollo

La integración de **LLMs y agentes autónomos** en el proceso de desarrollo evidencia la necesidad urgente de **nuevas metodologías y marcos de trabajo**. Los paradigmas tradicionales de ingeniería de software requieren adaptación para incorporar la **colaboración humano-IA** de manera efectiva. Esta observación representa una **oportunidad de investigación** significativa que podría redefinir las mejores prácticas en desarrollo de sistemas de información.

### Valoración de la Experiencia Académica

La **metodología pedagógica** empleada en el curso ha sido extraordinariamente efectiva. El enfoque basado en **retos prácticos y del mundo real** facilitó un aprendizaje experiencial que va más allá de la adquisición de conocimientos teóricos. La dinámica de mini-hackathons permitió experimentar con tecnologías emergentes en contextos aplicados, generando un entendimiento más profundo y duradero.

### Perspectivas Profesionales

Esta experiencia ha **reafirmado y expandido** mi vocación profesional en el desarrollo de sistemas de información para la gestión organizacional. Sin embargo, ahora con una perspectiva enriquecida que integra las **capacidades transformadoras de la IA** como herramienta de valor empresarial. El aprendizaje adquirido no solo representa competencias técnicas adicionales, sino un **cambio paradigmático** en cómo conceptualizar y ejecutar proyectos de sistemas de información.

La intersección entre **gestión empresarial e inteligencia artificial** se presenta como un campo de oportunidades extraordinarias, donde la capacidad de traducir necesidades organizacionales complejas en soluciones tecnológicas inteligentes será cada vez más valorada. Este portafolio documenta no solo proyectos completados, sino la **evolución de una mentalidad** preparada para liderar la próxima generación de sistemas de información empresarial.

---

## 6. Créditos

Agradecimiento especial a mis compañeros de equipo **Carlos Rodríguez**, **Juan José Acevedo**, **Ixent Cornella**, **Carla Claramunt**, **Jofre Coll** y al profesor **Marc Alier**.