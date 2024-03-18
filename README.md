# AKS-cluster-using-Terraform
A] Prerequisites
https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-windows?tabs=azure-cli
https://code.visualstudio.com/download
https://learn.microsoft.com/en-us/azure/developer/terraform/configure-vs-code-extension-for-terraform?tabs=azure-cli
https://developer.hashicorp.com/terraform/install
https://kubernetes.io/releases/download/ 

B] Create Resources using Terraform 
terraform init –upgrade 
terraform plan -out main.tfplan
terraform apply main.tfplan

C] Deploy Application

Kubectl apply –f deployment.yml
Kubectl apply –f service.yml
Kubectl get svc 

D] Cleanup

kubectl get all

kubectl delete service/swiggy-app

kubectl delete deployment.apps/swiggy-app

terraform plan -destroy -out main.destroy.tfplan 

terraform apply "main.destroy.tfplan"


Credit : Ashfaque 
