### Table of Contents

<img width="100" alt="logo" src="https://github.com/user-attachments/assets/0c9cf0c6-1b4f-40aa-b8da-07fac22a1650" />

Docker Compose v2
Where to Get Docker Compose
Windows and macOS
Linux
Quick Start
Contributing
Legacy
Docker Compose v2
Docker Compose es una herramienta para ejecutar aplicaciones multi-contenedor en Docker, definidas usando el formato de archivo Compose. Un archivo Compose se usa para definir cómo se configuran uno o más contenedores que forman tu aplicación. Una vez que tienes el archivo Compose, puedes crear y arrancar tu aplicación con un solo comando:

bash
Copiar código
docker compose up
GitHub Release, PkgGoDev, Build Status, Go Report Card, Codecov, OpenSSF Scorecard
Docker Compose GitHub Release
PkgGoDev
Build Status
Go Report Card
Codecov
OpenSSF Scorecard
Where to Get Docker Compose
Windows and macOS
Docker Compose está incluido en Docker Desktop para Windows y macOS. Al instalar Docker Desktop, Docker Compose se instalará automáticamente.

Linux
Puedes descargar los binarios de Docker Compose desde la página de releases de este repositorio.

Descarga el binario correspondiente a tu sistema operativo.

Renombra el archivo descargado a docker-compose.

Copia el binario a uno de los siguientes directorios para instalarlo de forma global:

$HOME/.docker/cli-plugins
/usr/local/lib/docker/cli-plugins o /usr/local/libexec/docker/cli-plugins
/usr/lib/docker/cli-plugins o /usr/libexec/docker/cli-plugins
Nota: Es posible que necesites dar permisos de ejecución al archivo con:

bash
Copiar código
chmod +x /path/to/docker-compose
Quick Start
El uso de Docker Compose es un proceso de tres pasos:

Define el entorno de tu aplicación con un Dockerfile para que pueda ser reproducido en cualquier entorno.

Define los servicios que componen tu aplicación en un archivo docker-compose.yaml para que puedan ser ejecutados juntos en un entorno aislado.

Finalmente, ejecuta el comando:

bash
Copiar código
docker compose up
Compose arrancará y ejecutará tu aplicación completa.

Ejemplo de archivo docker-compose.yaml:
yaml
Copiar código
services:
  web:
    build: .
    ports:
      - "5000:5000"
    volumes:
      - .:/code
  redis:
    image: redis
Contributing
¿Quieres ayudar a desarrollar Docker Compose? Consulta nuestra documentación para contribuir.

Si encuentras un problema, por favor repórtalo en el rastreador de problemas.

Legacy
La versión en Python de Docker Compose está disponible en la rama v1 de este repositorio.

