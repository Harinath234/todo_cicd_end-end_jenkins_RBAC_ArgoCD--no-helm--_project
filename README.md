## Project Structure

```text
todo-project
│
├── Jenkinsfile
├── Dockerfile
│
├── Kubernetes
│   ├── deployment.yaml
│   └── service.yaml
│
├── rbac
│   ├── namespace.yaml
│   ├── serviceaccount.yaml
│   ├── role.yaml
│   └── rolebinding.yaml
│
└── ansible
    ├── inventory
    └── deploy.yml
```
    

## Project Flow

```

GitHub
   ↓
Jenkins
   ↓
Build Docker Image
   ↓
Push Docker Image
   ↓
Update deployment.yaml
   ↓
Git Push
   ↓
Ansible Playbook
   ↓
Kubernetes (RBAC + Deployment + Service)

```
