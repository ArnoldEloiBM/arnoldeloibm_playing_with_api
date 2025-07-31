# Web Application

A simple web application served with Nginx in a Docker container.

## Prerequisites

- Docker installed on your system
- Git (for cloning the repository)

## Building and Running

### Build the Docker image

```bash
docker build -t my-web-app .
```

### Run the container

```bash
docker run -p 8080:8080 my-web-app
```

### Access the application

Open your web browser and navigate to:
```
http://localhost:8080
```

## Development

The application consists of:
- `index.html` - Main HTML file
- `style.css` - CSS styles
- `script.js` - JavaScript functionality
- `nginx.conf` - Nginx configuration

## Docker Commands

### Build with a specific tag
```bash
docker build -t my-web-app:latest .
```

### Run in detached mode
```bash
docker run -d -p 8080:8080 my-web-app
```

### Stop the container
```bash
docker stop <container_id>
```

### View running containers
```bash
docker ps
```

### View container logs
```bash
docker logs <container_id>
```

## Health Check

The container includes a health check that runs every 30 seconds to ensure the application is responding correctly.

## Port Configuration

The application runs on port 8080 by default. You can change this by modifying the `EXPOSE` directive in the Dockerfile and the `listen` directive in `nginx.conf`. 