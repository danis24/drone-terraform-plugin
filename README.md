# Drone Terraform Plugin

Drone terraform plugin is for provision and deploy with terraform

## Feature
- openssl (included)
- terraform <plan><apply>

## Usage
- Decrypt kube_secret with openssl `openssl enc -aes-256-cbc -d -in .kube_secrets.tar.enc -out .kube_secrets.tar -k $AES_PASSWORD`
- Extract tar to kubeconfig `tar -xvzf .kube_secrets.tar`
- `docker run danis24/drone-terraform-plugin:v1.0 terraform <command>`