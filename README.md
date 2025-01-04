Table of Contents
Docker Compose v2
Where to get Docker Compose
Windows and macOS
Linux
Quick Start
Contributing
Legacy
Docker Compose v2
GitHub release PkgGoDev Build Status Go Report Card Codecov OpenSSF Scorecard Docker Compose

Docker Compose is a tool for running multi-container applications on Docker defined using the Compose file format. A Compose file is used to define how one or more containers that make up your application are configured. Once you have a Compose file, you can create and start your application with a single command: docker compose up.

Where to get Docker Compose
Windows and macOS
Docker Compose is included in Docker Desktop for Windows and macOS.

Linux
You can download Docker Compose binaries from the release page on this repository.

Rename the relevant binary for your OS to docker-compose and copy it to $HOME/.docker/cli-plugins

Or copy it into one of these folders to install it system-wide:

/usr/local/lib/docker/cli-plugins OR /usr/local/libexec/docker/cli-plugins
/usr/lib/docker/cli-plugins OR /usr/libexec/docker/cli-plugins
(might require making the downloaded file executable with chmod +x)

Quick Start
Using Docker Compose is a three-step process:

Define your app's environment with a Dockerfile so it can be reproduced anywhere.
Define the services that make up your app in compose.yaml so they can be run together in an isolated environment.
Lastly, run docker compose up and Compose will start and run your entire app.
A Compose file looks like this:

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
Want to help develop Docker Compose? Check out our contributing documentation.

If you find an issue, please report it on the issue tracker.

Legacy
The Python version of Compose is available under the v1 branch.
