# AWS SRE Mini-Lab – David Njoku (Novembre 2025)

Mini-laboratoire SRE complet exécuté en live dans **AWS CloudShell**  
Objectif : pratiquer observabilité, conteneurs Kubernetes et automatisation cloud

## Fonctionnalités implémentées
- Kubernetes local avec **Minikube** (driver docker)
- **Prometheus** + **Grafana** pour le monitoring
- Exporter Python personnalisé (métriques CPU/Mémoire de CloudShell)
- Backup automatisé vers S3 avec PowerShell
- Application Nginx déployée dans Minikube

## Lancement complet (testé et validé dans AWS CloudShell)

```bash
# 1. Créer la structure
mkdir -p ~/aws-sre-lab/{monitoring,scripts,manifests} && cd ~/aws-sre-lab

# 2. Démarrer Minikube (Kubernetes)
minikube start --driver=docker

# 3. Lancer Prometheus + Grafana
docker-compose up -d

# 4. Lancer l'exporter Python (métriques en temps réel)
nohup python3 monitoring/monitor.py > monitor.log 2>&1 &

# 5. Déployer une app de test dans Kubernetes
kubectl apply -f manifests/nginx-deployment.yaml

# 6. Ouvrir les interfaces
#    Grafana → http://localhost:3000 (admin/admin)
#    Prometheus → http://localhost:9090
