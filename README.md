# Virtual Machine Quickstarts

Worked examples of Bicep and Terraform virtual machine quickstarts. These can be used to show the differences between the tooling and approaches.

---

## Terraform

<https://learn.microsoft.com/en-us/azure/virtual-machines/linux/quick-create-terraform>

Commands:

1. `terraform init`
1. `terraform plan -out main.tfplan`
1. `terraform apply main.tfplan`
1. `terraform destroy`

---

## Bicep

<https://learn.microsoft.com/en-us/azure/virtual-machines/linux/quick-create-bicep?tabs=CLI>

Commands:

1. `az group create --name rg-foxtrot-mike --location eastus`
1. `az deployment group create --resource-group rg-foxtrot-mike --template-file main.bicep --parameters adminUsername=vmaddy`
   1. You'll also be prompted to enter adminPassword. The minimum password length is 12 characters.
1. `az group delete --name rg-foxtrot-mike`
