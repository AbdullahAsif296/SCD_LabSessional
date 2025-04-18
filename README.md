# Cafe Management System

This directory contains the microservices and configuration files for the Cafe Management System.

## Directory Structure

- `api-gateway/`: API Gateway service
- `customer-services/`: Customer management service
- `inventory-services/`: Inventory management service
- `menu-services/`: Menu management service
- `order-services/`: Order management service
- `payment-services/`: Payment processing service
- `docker-compose.yml`: Docker Compose configuration for local development
- `docker-compose.prod.yml`: Docker Compose configuration for production deployment

## Local Development

Use the standard `docker-compose.yml` for local development:

```bash
docker-compose up --build
```

## Production Deployment

For production, use the `docker-compose.prod.yml` file, which uses pre-built Docker images from Docker Hub:

```bash
# Set your Docker Hub username
export DOCKERHUB_USERNAME=your-dockerhub-username

# Run with the production configuration
docker-compose -f docker-compose.prod.yml up -d
```

## CI/CD Pipeline

This project includes GitHub Actions workflows for CI/CD:

1. Automatically running tests
2. Building Docker images for all microservices
3. Pushing images to Docker Hub
4. Deploying to production or staging environments

See the `.github/workflows/` directory in the root of the repository for the workflow configurations and instructions.
