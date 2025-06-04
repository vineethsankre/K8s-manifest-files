# Voting App Kubernetes Manifests

This folder contains the Kubernetes manifests to deploy the Docker Voting App.

## Components
- `voting-app`: Frontend app
- `result-app`: Results UI
- `worker-app`: Backend processor
- `redis`: Queue
- `postgres`: Database

## How to Apply
```bash
kubectl apply -f namespace.yaml
kubectl apply -f .
