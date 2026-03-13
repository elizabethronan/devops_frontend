# Ecommerce Frontend

A React-based frontend for the ecommerce platform, served via Nginx.

## Technology Stack
- React 18
- Nginx (production server)
- Docker (containerized deployment)

## Local Development

### Prerequisites
- Node.js 22+
- npm

### Install Dependencies
```bash
npm install
```

### Run Development Server
```bash
npm start
```

Access the app at `http://localhost:3000`

### Run Tests
```bash
npm test
```

### Build for Production
```bash
npm run build
```

## Docker

### Build Image
```bash
docker build -t eronan22/ecommerce-frontend:latest .
```

### Run Container
```bash
docker run -p 3000:80 eronan22/ecommerce-frontend:latest
```

## Environment Variables
| Variable | Description | Default |
|----------|-------------|---------|
| REACT_APP_PRODUCT_SERVICE_URL | Product service URL | http://product-service:3001 |
| REACT_APP_ORDER_SERVICE_URL | Order service URL | http://order-service:3002 |

## CI/CD
This service uses a Jenkins pipeline defined in `Jenkinsfile`.
Pipeline stages: PR Validation → Build → Test → Security Scan → 
Container Build & Push → Deploy

## Docker Hub
```
eronan22/ecommerce-frontend
```