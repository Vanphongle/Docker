# Web Application Deployment with Docker
This repository contains files for setting up a Docker environment for a web application. The environment consists of two services: a reverse proxy service based on NGINX, and a web service based on Apache httpd.

The web application is built using a template from https://untree.co/cat/blog/.

## Requirements
Docker
Docker Compose
## Installation and Usage
1. Clone this repository to your local machine.
2. In a terminal, navigate to the root directory of the cloned repository.
3. Run the following command to build the Docker images and start the containers:

    ![image](https://user-images.githubusercontent.com/105464424/218635162-76f071d9-9c3d-47a1-a7ae-157a9367db18.png)
4. Access the web application by visiting http://localhost in your web browser.
# Configuration
## NGINX Configuration
The nginx.conf file in the root directory of the repository contains the configuration for the NGINX reverse proxy. It specifies that the server should listen on port 80 and forward requests to a service named "web" at http://web. It also includes some proxy headers to identify the original client IP and hostname.
## Docker Compose Configuration
The docker-compose.yml file defines two services: proxy and web. The proxy service is built using the nginx.Dockerfile and exposes port 80 to the host. The web service uses the httpd image and mounts the current directory (.) to the /usr/local/apache2/htdocs/ directory in the container. This likely means that the web content is served from the current directory.

# Contributing
Contributions are welcome! Please open an issue or pull request if you would like to contribute to this project.
