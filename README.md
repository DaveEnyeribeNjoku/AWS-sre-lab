
# AWS SRE Mini-Lab : Monitoring avec Prometheus + Grafana

Un lab complet de monitoring SRE (Site Reliability Engineering) qui déploie Prometheus, Grafana et un exporter Python custom pour surveiller les ressources système (CPU/RAM) dans AWS CloudShell ou n'importe quel environnement Linux avec Docker.

🎯 Objectifs du lab
🚀 Déployer un stack de monitoring moderne (Prometheus + Grafana)
📊 Exposer des métriques système via un exporter Python
📈 Visualiser les métriques dans Grafana avec des dashboards
💡 Apprendre les bases du monitoring SRE
🔧 Facilement reproductible dans n'importe quel environnement


Stack complète et reproductible en local ou sur AWS CloudShell.

## Lancement ultra-rapide (recommandé)
```bash
git clone https://github.com/DaveEnyeribeNjoku/aws-sre-lab.git
cd aws-sre-lab
cp .env.example .env
docker compose up -d --build   # ou docker-compose up -d
