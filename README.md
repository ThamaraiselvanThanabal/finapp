# Node.js API with Kubernetes Deployment

This is a simple Node.js API application configured for deployment on Kubernetes.

## Local Development

1. Install dependencies:

   ```bash
   npm install
   ```

2. Run the application:

   ```bash
   npm start
   ```

3. The API will be available at http://localhost:3000

## Docker

Build the Docker image:

```bash
docker build -t nodejs-api .
```

Run locally:

```bash
docker run -p 3000:3000 nodejs-api
```

## Kubernetes Deployment

1. Build and push the Docker image to your registry (update the image in deployment.yaml).

2. Apply the Kubernetes manifests:

   ```bash
   kubectl apply -f k8s/
   ```

3. Check the deployment:
   ```bash
   kubectl get pods
   kubectl get services
   ```

## API Endpoints

- GET / : Welcome message
- GET /api/health : Health check
