# Informe tecnico:Docker
--- 
**Video #1:** 

Este video ofrece una introducción clara y concisa a Docker como una plataforma para **crear**, **ejecutar** y **administrar** aplicaciones dentro de **contenedores**.
Los puntos a tener en cuenta:

- Un contenedor es una unidad ligera que incluye todo lo necesario para ejecutar una aplicación: código, librerías y dependencias.

- Docker permite garantizar que el software se ejecute igual en cualquier entorno.

- Las imágenes de Docker son plantillas inmutables usadas para crear contenedores.

- Un Dockerfile define los pasos para construir una imagen personalizada.

- Docker Hub actúa como repositorio público de imágenes.

**Video #2:**

Este video profundiza en la **práctica de crear y ejecutar contenedores.**
Conceptos importantes:

- Instalación básica de Docker en el sistema operativo.

- Comandos fundamentales:

    1. docker pull para descargar imágenes.

    2. docker run para ejecutar contenedores.

    3. docker ps para listar contenedores activos.

    4.  stop y docker rm para detener o eliminar contenedores.

    5. Creación de un Dockerfile para definir una aplicación propia.

- Uso de docker-compose.yml para orquestar múltiples servicios (por ejemplo, una app y su base de datos).



## Reflexiones 

**Ventajas:**
Docker simplifica la configuración de entornos y mejora la portabilidad de las aplicaciones. Es ideal para equipos de desarrollo, ya que asegura que todos trabajen en entornos idénticos.

**Desafíos:**
Requiere entender conceptos de redes, imágenes y capas. Los errores en la construcción de imágenes pueden generar mal uso de espacio o conflictos en las versiones.

**Uso práctico:**
Lo aplicaría en proyectos donde se necesiten varios servicios (por ejemplo, una API con base de datos y frontend) o donde deba asegurar que las pruebas se ejecuten igual en todos los entornos.
---
## Ejemplo practico: creando un hola mundo en docker

Dentro de vs Code crear archivo **"dockerfile"**
Como se muestra en la siguiente imagen:
<img width="702" height="489" alt="image" src="https://github.com/user-attachments/assets/a9889bb8-dcb1-4902-b60a-a8efe23692bb" />

Tambien un archivo .py 
Asi:
<img width="854" height="348" alt="image" src="https://github.com/user-attachments/assets/4d9057f0-bbb0-4f74-8666-5df8f57fb4ff" />

Luego ejecutar el comando:

``` bash
docker build -t miappdocker .
```
Para construir la imagen

Despues:
``` bash
docker run -p 5000:5000 miappdocker
```

Este para ejecutar el contenedor, y por ultimo abrir el navegador en http://localhost:5000, se mostrará el mensaje:
"¡Hola desde un contenedor Docker!"

<img width="548" height="247" alt="image" src="https://github.com/user-attachments/assets/9a377d58-1023-4b46-bde8-88aa1da8224c" />

---
## Consultas adicionales

- https://docs.docker.com/
- https://hub.docker.com/
- https://docs.docker.com/reference/cli/docker/
