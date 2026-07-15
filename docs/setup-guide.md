
# Environment Setup Guide

## EC2 Instance

| Setting | Value |
|---|---|
| Instance Type | t2.large |
| Region | us-east-1 |
| OS | Ubuntu 22.04 LTS |
| Storage | 20GB gp2 |

Minimum t2.large required — running Docker, kubectl, and Terraform 
simultaneously needs at least 8GB RAM.

## Tools Installed

### Docker
```bash
sudo apt update
sudo apt install docker.io -y
sudo systemctl enable docker
sudo usermod -aG docker $USER
```

### kubectl
```bash
curl -LO "https://dl.k8s.io/release/$(curl -L -s \
  https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
chmod +x kubectl
sudo mv kubectl /usr/local/bin/
```

### Terraform
```bash
wget https://releases.hashicorp.com/terraform/1.7.0/terraform_1.7.0_linux_amd64.zip
unzip terraform_1.7.0_linux_amd64.zip
sudo mv terraform /usr/local/bin/
```

## Verification

```bash
docker --version
kubectl version --client
terraform version
```
