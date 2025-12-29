# Home Kubernetes Cluster Project

A hands-on project to build and manage a Kubernetes cluster from scratch using Ubuntu VMs, Ansible for automation, and various Kubernetes features.

## Project Overview
This project demonstrates my practices on the following:
- Automated Kubernetes cluster setup using Ansible
- Multi-node cluster (1 control plane + 3 workers of ubuntu-24.04.3-live-server-amd64)
- Docker image creation for sample applications
- Kubernetes features: Networking, Ingress, Taints & Tolerations, Node Affinity
- CI/CD with GitHub Actions

## Technologies Used
- **Kubernetes**: Container orchestration
- **Ansible**: Infrastructure automation
- **Docker**: Containerization
- **Ubuntu Server**: Operating system
- **Calico**: Container Network Interface (CNI)
- **Nginx Ingress**: Ingress controller
- **GitHub Actions**: CI/CD automation

## Project Structure
```
My-Home-k8s-Cluster/
├── README.md
├── .gitignore
├── ansible/
│   ├── inventory/
│   │   └── hosts.ini
│   ├── group_vars/
│   │   ├── all.yml
│   │   ├── control_plane.yml
│   │   └── workers.yml
│   ├── roles/
│   │   ├── common/
│   │   ├── k8s-control-plane/
│   │   └── k8s-worker/
│   └── playbooks/
│       ├── 01-setup-prerequisites.yml
│       ├── 02-setup-control-plane.yml
│       └── 03-join-workers.yml
├── kubernetes/
│   ├── apps/
│   │   ├── app1/
│   │   └── app2/
│   ├── network/
│   └── storage/
├── docker/
│   ├── app1/
│   └── app2/
└── .github/workflows/
    ├── build-docker.yml
    └── deploy-k8s.yml
```

## Detailed Documentation
See [docs/](docs/) for step-by-step guides.
