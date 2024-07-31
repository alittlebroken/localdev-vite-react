# Vite React dev containers
A simple local development server utilising vite and React

The docker images use the local folder the docker-compose command 
is used from to persist the app code you develop.

## Tech stack

### Prerequisite
- Windows 11
- Docker Desktop

### Production
- vite
- react

### Development
- nodemon
- jest

## Installation

### NOTES
- Docker will give the parent name the same as the folder that the docker-compose comman was issued from
- The actual images will be named based on the service names you set in the docker compose yaml file

### Setup

- Clone the github repo
```cmd
git clone https://github.com/alittlebroken/localdev-vite-react.git
```

- Update project folder name
```cmd
ren localdev-vite-react <project_name>
cd <project_name>
```

- Update the remote git repo to your new repo location
```cmd
git remote set-url origin <new remote repo>
```

- Edit the docker-compose.dev.yaml file and set the service names to your desired names
- Add any environment vars or other options like mounted volumes that you require

- Build and start the docker image
```cmd
docker-compose -f docker-compose.dev.yaml up --build -d
```

- Start containers after first build
```cmd
docker-compose -f focker-compose.dev.yaml up -d
```

- Attach to an running container
```cmd
docker-compose -f docker-compose.dev.yaml exec <service name> bash
```

- Launch vscode
```cmd
code .
```