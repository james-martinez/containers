# containers
Intro to Containers and Orchestration

# Runtimes
- Docker engine
  - Comes with their networking, cli, and api. Community Edition (CE) free and Enterprise Edition (EE) paid. 
- Containerd and runc
  - donated by Docker to the Cloud Native Computing Foundation (CNCF).
- CRI-O 
  - Redhat
- rkt
  - CoreOS
- LXD
 - Linux Containers
# Containers vs Virtual Machines and Bare Metal
- Containers use Linux security primitives such as Linux kernel namespaces to sandbox different applications running on the same computers and control groups (cgroups), to avoid the noisy neighbor problem where one bad application is using all available resources of a server and starving all other applications.
- Containers are fast and ephemeral.
- Containers are not virtualized but still use isolation technology.
# Benefits:
- Gets rid of "pets"
- Productivity and efficiency boost vs standard computing methods.
  - Standardization
  - Porablility
  - Automation
  - Less maintenance
  - Faster delivery
# What makes a continer:
 - Uses a traditional linux root file system. /etc/ /usr/ /bin/
 - Can be one to many layers. Each individual layer contains files and folders
# Common base images
- Alpine
- Ubuntu
- UBI (Redhat), Redhat CoreOS, Fedora CoreOS
- CentOS
# Ways of creating:
- Start a base image, make changes, and save it final result. (Interactive, manual)
- Use a dockerfile, a recipe (Declarative, automated)
- Import an image from a tarball. Good for "offline" use where container registires are not implemented.
# Sharing and shipping:
- Container image registires
  - Public - Dockerhub, AWS Ecr, Google Gcr, Microsoft Acr, Quay, Gitlab, Github
  - Private (self hosted) - Nexus, Gitlab , Artifactory, Harbor, Standalone (Docker's image and nginx)
- Saving and importing
# Versioning
- Tags - Naming
- Hashes - Hash of image filesize
# Supported Architectures
- amd64
- arm64
- ppc64le
- s390x
# Orchestrators
- Kubernetes
- Docker Swarm
- Apache Mesos
- AWS Elastic Container Service (ECS)
- Microsoft Azure Container Service (ACS)
# Security
- Host based
  - AppArmor
  - SElinux
  - Seccomp
- Vulnerability and policy scanning tools
  - Prisma Cloud (Twistlock) 
  - OpenSCAP
- Virus scanning tools
  - Anchore
  - ClamAv
- Digital Signatures Admission Controllers, and enforcement 
  - Notary
  - TUF
  - OPA
- RBAC (Role Based Access Control) 
  - Kubernetes
  - Docker

# References:
- Gabriel N. Schenker, Hideto Saito, Hui-Chuan Chloe Lee, Ke-Jou Carol Hsu, Getting Started with Containerization, 2019

# Host Runtimes
- Linux
- Windows
- OSX

# Online Tools
- Gitpod
- Github Codespaces
- Eclipse Che
