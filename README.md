# 📄 Extractor y Clasificador de Currículums para convertirlo en Portafolio web con Gemini
Este proyecto es una aplicación desarrollada con **Google Gemini y LangChain**, diseñada para automatizar la **extracción de datos desde currículums PDF**, clasificarlos por perfil profesional y generar un **portafolio web editable para desarrolladores front-end**.

💡 El desarrollo surge como parte de la iniciativa **Imersão Dev Agentes de IA - Google + Alura (Brasil)**, y representa un caso práctico de cómo los agentes de IA pueden agilizar flujos de trabajo complejos, reduciendo drásticamente el tiempo de análisis, organización y estructuración de contenido profesional.

---

## ⚙️ Flujo del Proyecto: De PDF a Portafolio

### 1. 📥 Extracción del texto del PDF
Se utiliza `PyMuPDF` para extraer el contenido textual del currículum cargado por el usuario.

### 2. 🧠 Clasificación del perfil
Con ayuda de **embeddings y similitud de coseno**, se compara el contenido del CV contra perfiles de referencia definidos (por ejemplo, Tecnológico, Financiero, Salud, etc.), seleccionando el más cercano.

### 3. 🔍 Extracción de información clave con Gemini
Según el perfil detectado, se genera un **prompt dinámico** y se consulta a Gemini 1.5 Flash. El resultado es un **JSON estructurado** con los campos relevantes:

- Nombre, contacto, resumen, experiencia, educación, habilidades, etc.
- Validación con Pydantic para garantizar consistencia.

### 4. 🌐 Generación de un portafolio web editable
Se genera un archivo `.html` como plantilla editable que puede ser usado por un desarrollador front-end para personalizarlo según su estilo o branding.

✨ Esta versión editable está pensada como **punto de partida profesional**, no como producto final. Contiene la información estructurada en formato limpio y organizado para facilitar el trabajo posterior de maquetación.

---

## 🖥️ Interfaz con Gradio

El usuario puede:
- Subir su CV en formato PDF
- Ver el perfil clasificado
- Obtener una **vista previa del portafolio web**
- Descargar el HTML editable
- Acceder al **JSON estructurado** con todos los datos

---

## 📸 Capturas del Funcionamiento

| Google Colab | Interfaz Gradio |
|--------------|------------------|
| ![captura-colab-generador-de-portafolio](https://github.com/user-attachments/assets/aa9fdacd-1bc0-4569-808e-38364ddcff55) | ![captura-gradio-generador-de-portafolio](https://github.com/user-attachments/assets/1b070438-82b9-4362-af20-fdda33201512)
|

| JSON generado | Portafolio HTML generado |
|--------------|---------------------------|
| ![captura-Json-generador-de-portafolio](https://github.com/user-attachments/assets/086c7018-a0b0-4878-b477-3800d9012e90) | ![captura-web-generador-de-portafolio](https://github.com/user-attachments/assets/bb6e63fa-9e42-4b50-82b4-d6b172b55166)
|

---

## 🛠️ Estado del Proyecto

### ✅ Fase 1: lista
- Lectura de CVs en PDF
- Clasificación de perfil
- Extracción de datos con Gemini
- Visualización en interfaz Gradio
- Generación de HTML editable

### 🔧 Fase 2: en desarrollo
- Incorporación de CSS descargable junto al HTML
- Mejoras en estructura semántica del HTML
- Opciones para personalización visual (temas)
- Posible integración con repositorios de GitHub Pages

---

## 📬 Contacto

- ✉️ Email: [nattypavez@gmail.com](mailto:nattypavez@gmail.com)  
- 💼 LinkedIn: [linkedin.com/in/natalia-pavez-programacion](https://www.linkedin.com/in/natalia-pavez-programacion)  
- 🐙 GitHub: [github.com/NattyPavez](https://github.com/NattyPavez)  

---

✨ **Hecho con pasión por la IA, el diseño y el código.**

