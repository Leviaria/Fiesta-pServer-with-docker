## Prerequisites

* Docker
* Git

## Build

Clone the Fiesta Online P-Server repository:

```
git clone https://github.com/fiesta-p/fiesta-p-server.git
```

Change to the directory containing the Dockerfile.

```
cd fiesta-p-server/docker
```

Build the Docker image:

```
docker build -t fiesta-p-server .
```

## Run

Run the Docker image with:

```
docker run -d -p 80:80 fiesta-p-server
```

## Access

The server is now running and accessible at port 80 of your machine. You can connect to it with any Fiesta Online P-Client.