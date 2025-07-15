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

##🧩 2. O que preciso instalar ANTES de começar?

      | Ferramenta       | Finalidade                                        | Instalação (Linux/WSL/Mac)                                                                   |          |
      | ---------------- | ------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------- |
      | Docker           | Para construir e subir imagens das apps           | [https://docs.docker.com/get-docker/](https://docs.docker.com/get-docker/)                   |          |
      | Minikube ou Kind | Para rodar o cluster Kubernetes localmente        | [https://minikube.sigs.k8s.io/docs/start/](https://minikube.sigs.k8s.io/docs/start/)         |          |
      | kubectl          | Para interagir com o cluster Kubernetes           | `sudo apt install kubectl` ou veja o [site oficial](https://kubernetes.io/docs/tasks/tools/) |          |
      | Git              | Para versionar e subir o projeto no GitHub        | `sudo apt install git`                                                                       |          |
      | base64           | Para codificar secrets do banco (já vem no Linux) | \`echo -n 'valor'                                                                            | base64\` |

  

# Estrutura
      projeto-k8s-deploy/
      │
      ├── namespace.yaml
      ├── ingress/
      │   └── ingress.yaml
      │
      ├── database/
      │   ├── pvc.yaml
      │   ├── secret.yaml
      │   └── statefulset.yaml
      │
      ├── backend/
      │   ├── configmap.yaml
      │   ├── deployment.yaml
      │   └── Dockerfile
      │
      ├── frontend/
      │   ├── deployment.yaml
      │   └── Dockerfile
      │
      └── README.md


## Como rodar
1. Clonar o repositório:
```bash  
git clone <link-do-repositorio>  
cd projeto-k8s-deploy  
