
# Deploy OwnCloud Infinite Scale with Nginx Reverse Proxy

This repository provides all the necessary configuration files to deploy **OwnCloud Infinite Scale (OCIS)** using **Docker Compose** with an Nginx reverse proxy. It also includes configurations for SSL (managed by Certbot) and unlimited upload size. 

## Features
- **OwnCloud Infinite Scale** deployment using Docker Compose.
- Nginx reverse proxy setup with SSL via Let's Encrypt.
- Keycloak integration for Identity and Access Management (IAM).

## Prerequisites
1. Docker and Docker Compose installed.
2. A valid domain name (e.g., `cloud.example.com`) with DNS pointing to your server.
3. SSL certificates managed by Certbot.

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/mitexleo/ocis_docker.git
cd ocis_docker 
```

### 2. Configure Environment Variables
Update the environment variables in the `docker-compose.yml` and `Nginx` configuration files to match your setup (e.g., domain name, paths, etc.).

### 3. Start the Services
Run the following command to start the containers:
```bash
docker compose up -d
```

### 4. Obtain SSL Certificates (if not already done)
Use Certbot to issue SSL certificates for your domain. Ensure the paths to certificates match in the Nginx configuration file.

### 5. Access the Application
Navigate to your domain (e.g., `https://cloud.example.com`) to access OwnCloud Infinite Scale.

## Identity Management with Keycloak
This setup integrates **Keycloak** as the Identity Management (IDM) solution for OCIS. Check out my **Keycloak setup repository** for more details: [docker_keycloak](https://github.com/mitexleo/docker_keycloak).

## Contributing
Feel free to open issues or submit pull requests if you have suggestions or improvements.

## Support
If you find this repository helpful, consider [buying me a coffee](https://www.buymeacoffee.com/mitexleo) to support my work. Your support keeps me motivated to create and share more projects like this!
