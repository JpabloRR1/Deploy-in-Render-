# 🧠 Machine Learning API - Docker + Render Deployment

Este proyecto contiene una API REST desarrollada con **Flask** que permite exponer un modelo de Machine Learning para realizar predicciones.  
La aplicación está contenida en **Docker** para facilitar su ejecución en cualquier entorno y puede desplegarse fácilmente en servicios como **Render**.

## 🚀 ¿Qué hace esta API?

Empaqueta una aplicación Flask que sirve un modelo de Machine Learning a través de una interfaz HTTP.  
El uso de Docker garantiza que la aplicación funcione de forma consistente sin importar el sistema operativo o la configuración del equipo donde se ejecute.

## 📁 Estructura del Proyecto

La carpeta principal contiene:

- `app.py`: lógica principal de la API.
- `models/`: carpeta con los modelos entrenados.
- `Dockerfile`: define cómo construir la imagen del contenedor.
- `docker-compose.yml`: facilita el levantamiento del servicio completo.

## 🐳 Cómo usar esta API con Docker

1. Asegúrate de tener **Docker** y **Docker Compose** instalados.
2. Abre una terminal en la carpeta del proyecto.
3. Ejecuta el siguiente comando:

docker-compose up --build

4. Una vez iniciado el contenedor, accede a:

http://localhost:5001


Con esto, la aplicación Flask queda levantada dentro de un contenedor y puedes empezar a realizar peticiones HTTP para interactuar con el modelo.

## ☁️ Despliegue en Render

Para llevar la aplicación a producción:

1. Crea un repositorio en GitHub con el contenido del proyecto.
2. Asegúrate de agregar `gunicorn` al archivo `requirements.txt`, ya que Render lo utiliza para ejecutar aplicaciones Python en producción.
3. Regístrate en [render.com](https://render.com) y crea un nuevo servicio web.
4. Vincula tu cuenta de GitHub y selecciona el repositorio del proyecto.
5. Configura el servicio como una aplicación Python:
   - **Build Command**: `pip install -r requirements.txt`
   - **Start Command**: `gunicorn app:app`
6. Selecciona el plan gratuito y despliega.

Una vez finalizado el despliegue, obtendrás una **URL pública** desde donde podrás acceder a tu API de forma remota.

## 🧪 Pruebas

Puedes probar la API usando herramientas como **Postman**.  
Solo cambia la URL local (`http://localhost:5001`) por la URL pública proporcionada por Render.  
Desde allí podrás hacer peticiones HTTP y obtener respuestas del modelo de Machine Learning cargado.

## ✅ Requisitos del Proyecto

- Python 3.10  
- Flask  
- scikit-learn  
- joblib  
- gunicorn 



