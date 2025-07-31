#  Explore Countries

## Introduction

Tired of carrying heavy geography books? Welcome to the **Explore Countries** - your digital companion for exploring the world's countries! This interactive web application transforms the traditional way of learning about countries from static textbooks into an engaging, dynamic experience.

Instead of flipping through pages, you can now:
- **Search** for any country instantly
- **Filter** by region, population size, or alphabetical order
- **Explore** detailed information including flags, capitals, and population data

This project demonstrates how modern web technologies can make education more accessible and engaging, replacing the need for physical reference materials with a responsive, always-available digital solution.

## Features

- **Real-time Search**: Find any country by name with instant results
- **Smart Filtering**: Filter countries by region, population size, or first letter
- **Visual Learning**: High-quality country flags and organized data presentation
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- **Interactive Cards**: Click to highlight and focus on specific countries
- **Population Categories**: Small (<1M), Medium (1M-10M), Large (10M-100M), Huge (>100M)

## Technologies Used

- **Frontend**: HTML5, CSS3, JavaScript 
- **API**: [REST Countries API](https://restcountries.com/) - Free, comprehensive country data
- **Containerization**: Docker Hub
- **Deployment**: Render (Cloud Platform)
- **Load Balancer**: New repo to help (https://github.com/ArnoldEloiBM/arnoldeloibm-lb)

## API Documentation

This project utilizes the [REST Countries API](https://restcountries.com/), a free and comprehensive API that provides and it doesn't require the key:
- Country names, capitals, and regions
- Population data
- Country flags (PNG format)
- And much more country information

**API Endpoint Used**: `https://restcountries.com/v3.1/all?fields=name,capital,population,flags,region`

##  Running Locally

### Prerequisites
- Docker installed on your system
- Git (for cloning the repository)

### Quick Start
```bash
# Clone the repository
git clone https://github.com/ArnoldEloiBM/arnoldeloibm_playing_with_api
cd arnoldeloibm_playing_with_api

# Build the Docker image
docker build -t arnoldeloibm/my-web-app-countries:v1 .

# Run the container
docker run -p 8080:8080 arnoldeloibm/my-web-countries:v1

# Access the application
# Open your browser and navigate to: http://localhost:8080
```


##  Deployment to Render

### Why Render Instead of Waka Repo?

The deployment process presented significant challenges with the traditional Waka repository approach. The complexity of server configuration, manual setup, and maintenance overhead led to choosing **Render** as a more efficient alternative.

### Render Deployment Process

1. **Containerized Application**: The application is packaged using Docker for consistent deployment
2. **Automatic Scaling**: Render provides automatic scaling and load balancing
3. **Zero-Downtime Deployments**: Updates are deployed seamlessly without service interruption
4. **Built-in SSL**: Automatic HTTPS certificate management
5. **Environment Management**: Easy configuration through Render's environment variables interface

### Deployment Steps
1. Connect your GitHub repository to Render
2. Configure as a **Web Service**
3. Fill the form where you are asked to add your docker image
4. Fill the form and then click deploy and it it automatically deployed.
5. Repeate the steps for the second web server

**Live Application**: [(https://my-web-app-countries-v1-1.onrender.com/)] [(https://my-web-app-countries-v1.onrender.com/)]

## Load Balancer Implementation

For high availability and performance, this project includes a custom load balancer that distributes traffic across multiple web servers.

**Load Balancer Repository**: [(https://github.com/ArnoldEloiBM/arnoldeloibm-lb)]

The load balancer ensures:
- **High Availability**: Traffic distribution across multiple servers
- **Fault Tolerance**: Automatic failover if one server goes down
- **Performance**: Reduced response times through load distribution
- **Scalability**: Easy addition of new servers as demand grows

## Demo Video

**Project Demo**: [(https://youtu.be/WUS7oy2tWqg)]

The demo showcases:
- Application features and functionality
- Deployment process
- Load balancer configuration
- Performance testing

## Challenges & Solutions

### Challenge 1: Complex Waka Repository Deployment
**Problem**: The traditional Waka repository deployment required extensive server configuration, manual setup, and ongoing maintenance.

**Solution**: Migrated to Render's containerized deployment platform, which provides:
- Automated deployment pipelines
- Built-in monitoring and logging
- Simplified configuration management
- Reduced operational overhead

### Challenge 2: Port Conflicts in Local Development
**Problem**: Multiple Docker containers competing for the same ports during local testing.

**Solution**: Implemented flexible port mapping and container management:
- Dynamic port assignment
- Container lifecycle management
- Clear documentation for port conflicts

## Credits & Acknowledgments

- **REST Countries API**: [https://restcountries.com/](https://restcountries.com/)  Providing comprehensive country data
- **Render**: [https://render.com/](https://render.com/) Cloud deployment platform
- **Docker**: [https://hub.docker.com/](https://hub.docker.com/) - Containerization technology