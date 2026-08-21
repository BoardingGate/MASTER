# 📚 BoardingGate — Simulador de Oposiciones & Tutoría con IA

<p align="center">
  <img src="https://img.shields.io/badge/Oposiciones-Exam%20Simulator-2563EB?style=for-the-badge&logo=academia&logoColor=white" alt="Exam Simulator" />
  <img src="https://img.shields.io/badge/React%2018-SPA-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React 18" />
  <img src="https://img.shields.io/badge/AI-Gemini%20%2B%20OpenRouter-8B5CF6?style=for-the-badge&logo=openai&logoColor=white" alt="AI Engine" />
  <img src="https://img.shields.io/badge/PDF.js-Client--Side%20OCR-E11D48?style=for-the-badge&logo=adobeacrobatreader&logoColor=white" alt="PDF.js" />
  <img src="https://img.shields.io/badge/Storage-IndexedDB%20v6-34A853?style=for-the-badge&logo=databricks&logoColor=white" alt="IndexedDB" />
  <img src="https://img.shields.io/badge/Zero_Install-Single_File-4CAF50?style=for-the-badge" alt="Zero Dependencies" />
</p>

<p align="center">
  <b>BoardingGate Oposiciones Pro</b> es una plataforma integral de entrenamiento para oposiciones, másteres y exámenes oficiales. Genera simulacros realistas a partir de <b>tus propios temarios en PDF, convocatorias oficiales e Internet</b>, asistido por modelos avanzados de Inteligencia Artificial con análisis de debilidades y tutoría adaptativa.
</p>

<p align="center">
  <a href="#-características-principales">Características</a> •
  <a href="#-módulos-del-sistema">Módulos</a> •
  <a href="#-motor-de-ia-y-generación-de-preguntas">Motor de IA</a> •
  <a href="#-procesamiento-de-archivos-y-almacenamiento">Almacenamiento Local</a> •
  <a href="#-despliegue-y-uso-local">Instalación</a> •
  <a href="#-privacidad-y-datos">Privacidad</a>
</p>

---

## 🚀 Características Principales

├── 📑 Ingestión de PDFs y Documentos (Extracción de texto cliente con PDF.js)
├── ⚖️ Baremo de Examen 100% Configurable (Puntos acierto, fallo, blanco y
méritos) ├── 🎯 Simulacros en Tiempo Real con Cola Asíncrona (Sin pausas entre
preguntas) ├── ⏱️ Control de Ritmo & Desviación de Tiempo (Ahead/Behind schedule
en vivo) ├── 🧠 Ampliación de Conocimiento IA (Deep Dive inmediato en fallos) ├──
📊 Estadísticas y Fórmulas de Convocatoria (Ponderación examen + méritos) ├── 📈
Gráficas SVG de Evolución Histórica (Comparativa vs cortes oficiales) ├── 🔄
Simulacros de Refuerzo Personalizados (Entrenamiento focalizado en debilidades)
└── 🗄️ Persistencia Segura y Ligera (IndexedDB + exportación e importación
JSON)


---

## 🏛️ Módulos del Sistema

### 1. 📖 Gestión de Materias (`SubjectsTab`)
* **Configuración del Tribunal:** Define el número de preguntas, opciones por pregunta (3, 4 o 5), tiempo límite en minutos y porcentaje de nota de corte.
* **Baremo de Calificación Personalizado:** Puntuación por acierto ($+$), penalización por error ($-$) y puntuación por respuesta en blanco.
* **Fórmula de Concurso-Oposición:** Configuración de la ponderación de la fase de examen (ej. 90%), expediente académico/carrera (nota y multiplicador) y puntos de méritos extra.
* **Convocatoria Oficial Real:** Localización automática y vinculación con la última convocatoria oficial (fecha, plazas ofertadas, puntos de corte y descarga de exámenes previos).
* **Distribución de Pesos del Examen (Total 100%):**
  * **Documentos PDF Propios:** Sube leyes, temarios y resúmenes con asignación de porcentaje específico.
  * **Examen Oficial Previo:** Ponderación asignada a preguntas extraídas de convocatorias anteriores.
  * **Temario Abierto en Internet / IA:** Generación automática de temas con pesos personalizados mediante IA.

---

### 2. 📝 Simulador de Examen en Vivo (`ExamTab`)
* **Generación en Cola Asíncrona:** El sistema solicita bloques de preguntas en segundo plano mientras respondes, eliminando los tiempos de espera y garantizando una experiencia fluida.
* **HUD de Control en Vivo:**
  * **Temporizador con indicador de ritmo:** Cálculo de adelanto/retraso en minutos respecto al tiempo medio por pregunta.
  * **Panel de Netas:** Cálculo en directo de preguntas netas (Aciertos $-$ Fallos).
  * **Barra de Corte Dinámica:** Posición en tiempo real respecto al techo de examen, corte oficial y puntos acumulados.
* **Ampliación de Conocimiento (IA Deep Dive):** Al fallar una pregunta, pulsa el botón de ampliación para recibir una explicación pedagógica instantánea con fundamento teórico y claves de memorización.
* **Mapa de Navegación de Preguntas:** Rejilla visual con código de colores para revisar, saltar o responder cualquier pregunta del simulacro.

---

### 3. 📊 Histórico y Tutoría Adaptativa (`HistoryTab` & `AIAnalysis`)
* **Cuadro de Mando Histórico:** Registro exhaustivo de simulacros con desglose de aciertos, fallos, omisiones, tiempo invertido, netas y nota final ponderada.
* **Filtrado Avanzado por Fuentes y Temas:** Aísla el rendimiento por PDF específico, examen oficial o concepto del temario.
* **Tutoría con IA:**
  * **Detección de Fortalezas y Debilidades:** Clasificación automática de los temas con mejor y peor porcentaje de acierto.
  * **Consejos Pedagógicos:** Diagnóstico de estrategia de estudio en 3 puntos clave.
  * **Generador de Exámenes de Refuerzo:** La IA analiza tus fallos y crea una distribución de pesos optimizada para atacar tus puntos débiles.
* **Consolidación de Datos Huérfanos:** Asistente para fusionar o reactivar temas antiguos en caso de que modifiques el nombre del temario.
* **Gráfica de Evolución Histórica (SVG):** Visualizador de rendimiento con líneas de corte objetivo, techo de examen y media consolidada.

---

### 4. ⚙️ Ajustes y Configuración IA (`SettingsTab`)
* **Enrutador Multimodelo Inteligente:**
  * **Google Gemini (Direct API):** Compatible con `gemini-3-flash-preview`, `gemini-3-pro-preview`, `gemini-2.5-flash`, etc., con opción de búsqueda web.
  * **OpenRouter API:** Acceso a decenas de modelos (Claude 3.5 Sonnet, GPT-4o, DeepSeek R1/V3, Llama 3, Kimi K2.5).
  * **Modo Sin API (Bypass):** Opción para generar y copiar el prompt estructurado directamente sin coste de API.
* **Descubridor Dinámico de Modelos:** Búsqueda en vivo de modelos en OpenRouter con ordenación por coste (gratis vs pago), tamaño de ventana de contexto ($k$) y proveedor.
* **Copias de Seguridad Ligeras (JSON):** Exporta e importa toda tu configuración, materias y notas para traspasar tus datos entre ordenadores o navegadores.

---

## 🧠 Motor de IA y Generación de Preguntas

El simulador utiliza un sistema de prompts estructurado con validación estricta de formato JSON:

[Usuario / Materia] ──> [Prompt Engine] ──> [API Gemini / OpenRouter] │
[Simulador Activo] <── [JSON Parser] <── [Preguntas + Opciones + Feedback]


* **Dificultad Calibrada:** Las preguntas se generan con distractores plausibles y justificaciones detalladas basadas en jurisprudencia, normativa o literatura técnica.
* **Alineación con Temarios:** Si subes un PDF, la IA extrae los conceptos exclusivamente de ese documento para evitar preguntas fuera de programa.

---

## 🗄️ Procesamiento de Archivos y Almacenamiento

* **Extracción 100% en el Navegador:** El procesamiento de PDFs se realiza en local mediante **PDF.js**, sin enviar tus archivos a servidores de terceros para su lectura.
* **IndexedDB v6:** Los documentos extensos se almacenan en el almacenamiento estructurado de tu navegador para un acceso instantáneo entre sesiones.
* **Compatibilidad de Formatos:** Admite archivos `.pdf` (con capa de texto digital) y archivos de texto plano `.txt`.

---

## 🚀 Despliegue y Uso Local

**Zero-Build:** La aplicación no requiere `Node.js`, `npm`, Webpack ni compiladores externos.

### 1. Ejecución Local
```bash
# Clona el repositorio
git clone https://github.com/tu-usuario/boardinggate-oposiciones.git
cd boardinggate-oposiciones

# Abre el archivo index.html en cualquier navegador moderno

2. Despliegue en GitHub Pages

1.  Sube index.html a tu repositorio de GitHub.
2.  Ve a Settings > Pages y activa el despliegue desde la rama main.
3.  Accede a tu simulador desde tu ordenador, tablet o móvil.

🔒 Privacidad y Seguridad

  - Sin Base de Datos Externa: Todos tus temarios, notas, historiales y
    resultados se guardan exclusivamente en tu navegador (localStorage e
    IndexedDB).
  - Control de Claves: Tus claves API de Google Gemini y OpenRouter permanecen
    almacenadas en tu dispositivo y solo se comunican con los endpoints
    oficiales de cada proveedor.

⚖️ Aviso Legal

Esta aplicación es una herramienta de asistencia al estudio y autoaprendizaje.
Las preguntas generadas por los modelos de Inteligencia Artificial deben
contrastarse con los boletines oficiales del Estado, normativas vigentes y
temarios oficiales de la convocatoria correspondiente.
