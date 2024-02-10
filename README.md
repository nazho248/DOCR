![icon](https://github.com/nikolliervin/blast-ocr-extension/assets/45341025/e569385a-2bea-4380-9dda-4c4e6c1308a2)

# Blast OCR Chrome Extension

The Blast OCR Chrome Extension allows you to extract text from images using the [Blast OCR API Repository](https://github.com/nikolliervin/blast). Simply upload an image from your computer, and the extension will send the image to the Blast OCR API for processing, returning the extracted text.

Esta extension se esta desarrollando para sacar numeros y hacer operaciones con ellos o extraer textos de imagenes.

## Como usar


1. ### Instalacion

   - Descargar el repositrio en linea.
   - Descomprimir la carpeta con los archivos en algun lado donde no se vaya a borrar (el navegador necesita los archivos).
   - Abrir el navegador y entrar a `chrome://extensions/`.
   - Activar el modo desarrollador.
   - Clickear en `Cargar descomprimido` y seleccionar la carpeta con los archivos.
   - Listo, ya deberia estar instalada la extension.

2. ### Configuracion del servidor
El servidor se encarga de recibir las imágenes y enviarlas a la API de Blast OCR para que sean procesadas.

El servidor necesita Python y Uvicorn para funcionar, instalarlos y instalar algunas librerías.

Además de esto necesita descargar [Blast OCR API](https://github.com/nikolliervin/blast) que contiene archivos para ejecutar el servidor, enrutamiento y etc. y ejecutar una <b>consola de comandos</b> en modo administrador.
- Instalar Python desde la pagina oficial.
- Instalar Uvicorn con el comando `pip install uvicorn`.
- Instalar FastAPI con el comando `pip install fastapi`.
- instalar middleware con el comando `pip install fastapi.middleware.cors`.
- descargar Tesserract (es un instalable) desde [la pagina de instalación](https://tesseract-ocr.github.io/tessdoc/Installation.html), o mirar el [repositorio](https://github.com/tesseract-ocr/tesseract?tab=readme-ov-file#installing-tesseract) para mas informacion.
- Ya se puede arrancar el servidor con
``` py
python -m uvicorn main:app --reload`
```

2. **Procesr los datos con Blast OCR API:**
   - La extension enviará la imagen a la API de Blast OCR para que sea procesada en loca (127.0.0.1:8000).

3. **Tratar los datos**
   - La extension mostrara el texto extraido en un cuadro de texto.
