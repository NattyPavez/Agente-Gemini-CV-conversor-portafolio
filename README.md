# 📄 Extractor y Clasificador de Currículums con Gemini

Este proyecto es una aplicación desarrollada con **Google Gemini** y **LangChain** para automatizar la extracción y clasificación de datos de currículums en formato PDF.  

💡 El desarrollo surge como un proyecto paralelo a mi participación en la **Imersão Dev Agentes de IA Google**, una iniciativa de **Alura (Brasil)** en colaboración con **Google**.  

El objetivo es demostrar cómo los **agentes de IA** pueden agilizar flujos de trabajo complejos, reduciendo drásticamente el tiempo que requerirían tareas manuales de toma de decisiones y organización de información.

---

## ⚙️ Lógica del Proyecto: Un Flujo de Trabajo Modular

El sistema está diseñado en una serie de pasos lógicos y secuenciales, cada uno con una función específica:

### 1. 📥 Extracción de Datos de Origen
- Lectura del archivo PDF con **PyMuPDF (fitz)**.  
- Se obtiene el texto completo del currículum como fuente para el análisis posterior.  

### 2. 🧩 Clasificación de Perfil mediante Embeddings
- Se definen perfiles de referencia (ejemplo: *Tecnológico*, *Financiero*).  
- Con el **modelo de incrustaciones (embeddings_model)** de Gemini:  
  - Se convierten tanto los perfiles de referencia como el texto del CV en vectores numéricos.  
  - Se calcula la similitud del coseno para determinar el perfil más cercano.  

✨ Este paso establece el **contexto** para una extracción más precisa.

### 3. 🔍 Extracción de Datos con un Prompt Dinámico
- Una vez detectado el perfil, se invoca **Gemini 1.5 Flash**.  
- Se utiliza un **prompt dinámico** que se adapta al perfil clasificado:  
  - Si es *Tecnológico* → extrae lenguajes de programación, frameworks, proyectos relevantes.  
  - Si es *Otro perfil* → extrae nombres de empresas, experiencias y habilidades clave.  
- La salida se valida contra un **esquema de Pydantic**, asegurando consistencia en formato **JSON estructurado**.  

### 4. 🖥️ Interfaz de Usuario con Gradio
El usuario puede:  
- Subir un archivo PDF fácilmente.  
- Visualizar tanto la **clasificación del perfil** como los **datos extraídos** en un JSON ordenado.  

---

## 🚀 Fases del Proyecto
Este es solo el **primer paso** de una iniciativa más amplia:  
- 🛠️ Fase 1 (actual): extracción y clasificación de CVs.  
- 🎨 Fase 2 (en desarrollo): generar automáticamente un **portafolio web editable** a partir de los datos extraídos, optimizando el trabajo para que la creatividad y criterio humano se enfoquen en el diseño final.  

---

## 🎥 Video Demo
🎥 [Ver demo en video](https://github.com/NattyPavez/Agente-Gemini-CV-conversor-portafolio/raw/main/Demo-agente-gemini-colab.mp4)


---

## 📬 Contacto
Si quieres conversar sobre el proyecto, colaborar o dar feedback:  

- ✉️ **Email:** [nattypavez@gmail.com]  
- 💼 **LinkedIn:** [https://www.linkedin.com/in/natalia-pavez-programacion/](#)  
- 🐙 **GitHub:** [github.com/NattyPavez](https://github.com/NattyPavez)  

---
✨ *Hecho con pasión por la IA y el código.*
