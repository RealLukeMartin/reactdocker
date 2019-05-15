# React Docker

## Requirements
- docker
- docker-compose (Comes installed with docker on Docker for Mac and Docker for Windows)

## Usage

### Quick Demo
File changes won't update, just will get the app running to look at in the browser

`git@github.com:RealLukeMartin/reactdocker.git`

`cd reactdocker`

`docker-compose up`

### Development
File changes will update

`docker build -f Dockerfile.dev .`

At the end of the docker build command that you just ran a container id will output at the end. Use that at the end of the next command in place of [Container ID].

`docker run -p 3000:3000 -v /app/node_modules -v $(pwd):/app [Container ID]`