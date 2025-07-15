# Projeto-Deploy-Aplica-o-Kubernetes
**rascunho**
## Objetivo
Implementar uma aplicação fullstack com alta disponibilidade, persistência e acesso externo via Ingress, usando Kubernetes.

## Arquitetura
- Frontend React (Deployment + Service)
- Backend Flask (Deployment + Service)
- Banco PostgreSQL (StatefulSet + PVC + Secret)
- Ingress NGINX para rotas `/` e `/api/`
- ConfigMaps e Secrets para variáveis de ambiente

## Como rodar
1. Clonar o repositório:
```bash  
git clone <link-do-repositorio>  
cd projeto-k8s-deploy  
