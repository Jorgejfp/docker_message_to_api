# docker_message_to_api
![Descripción de la Imagen](https://github.com/jorgejfp/docker_message_to_api/blob/main/image.png?raw=true)


Author: Jorge

Docker Message to API
Este proyecto contiene un script que envía información del sistema a una API remota utilizando Docker. El contenedor Docker ejecuta un script en bash que envía un mensaje y la información del sistema en formato JSON a una API REST.

Estructura del Proyecto
.gitignore: Archivo que especifica qué archivos deben ser ignorados por Git. Por ejemplo, archivos .env y archivos .txt.
Dockerfile: Archivo de configuración para construir la imagen Docker.
post_message.sh: Script bash que envía una solicitud POST a una API con información del sistema.
Archivos
.gitignore
Este archivo asegura que algunos archivos sensibles o no necesarios no se incluyan en el control de versiones. Actualmente ignora:

Archivos .txt
Archivos .env
Dockerfile
El Dockerfile contiene las instrucciones necesarias para construir una imagen Docker que ejecute el script post_message.sh.

# Dockerfile example content (resumen del archivo real)
FROM alpine:3.12

RUN apk add --no-cache bash curl

COPY post_message.sh /usr/local/bin/post_message.sh
RUN chmod +x /usr/local/bin/post_message.sh

CMD ["/usr/local/bin/post_message.sh"]
>>>>>>> a488a8c0254ee068c1da0d82220179bd10a8874f
