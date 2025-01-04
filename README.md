### Tabla de Contenido  :<br>

<img width="100" alt="logo" src="https://github.com/user-attachments/assets/0c9cf0c6-1b4f-40aa-b8da-07fac22a1650" />

### Docker Compose v2
Where to Get Docker Compose
### Windows and macOS
### Linux
Quick Start
Contributing
Legacy
### Docker Compose v2
Docker Compose is a tool for running multi-container applications in Docker, defined using the Compose file format. A Compose file is used to define how one or more containers that make up your application are configured. Once you have the Compose file, you can create and start your application with a single command:

bash


## docker compose up



GitHub Release, PkgGoDev, Build Status, Go Report Card, Codecov, OpenSSF Scorecard
Docker Compose GitHub Release
PkgGoDev
Build Status
Go Report Card
Codecov
OpenSSF Scorecard
Where to Get Docker Compose
Windows and macOS
Docker Compose is included with Docker Desktop for Windows and macOS. By installing Docker Desktop, Docker Compose will be automatically installed.

Linux
You can download Docker Compose binaries from the release page of this repository.

Download the binary corresponding to your operating system.

Rename the downloaded file to docker-compose.

Copy the binary to one of the following directories for global installation:

$HOME/.docker/cli-plugins
/usr/local/lib/docker/cli-plugins or /usr/local/libexec/docker/cli-plugins
/usr/lib/docker/cli-plugins or /usr/libexec/docker/cli-plugins
Note: You may need to grant execute permissions to the file with:


bash


## chmod +x /path/to/docker-compose



## Quick Start
Using Docker Compose is a three-step process:

Define your application's environment with a Dockerfile so that it can be reproduced anywhere.

Define the services that make up your app in a docker-compose.yaml file so they can run together in an isolated environment.

Finally, run the following command:

bash

docker compose up



Compose will start and run your entire application.

Example docker-compose.yaml file:

yaml



services:
  web:
    build: .
    ports:
      - "5000:5000"
    volumes:
      - .:/code
  redis:
    image: redis





## Contributing
Want to help develop Docker Compose? Check out our contributing documentation.

If you find an issue, please report it on the issue tracker.

## Legacy
The Python version of Docker Compose is available in the v1 branch of this repository.














