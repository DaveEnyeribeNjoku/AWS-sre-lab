# AWS SRE Mini-Lab – David Njoku (Nov 2025)

Mini-laboratoire SRE complet sur laptop personnel  
Objectif : pratiquer observabilité, conteneurs et automatisation cloud

## Stack utilisée
- Minikube (Kubernetes local)
- Prometheus + Grafana (monitoring)
- Python custom exporter
- PowerShell script → backup fichiers vers S3
- Nginx simple déployé dans K8s

## Lancement rapide
```bash
# 1. Démarrer Minikube
minikube start --driver=docker

# 2. Stack monitoring
docker-compose up -d

# 3. Déployer l'app de test
kubectl apply -f manifests/nginx-deployment.yaml

# 4. Ouvrir Grafana → http://localhost:3000 (admin/admin)
