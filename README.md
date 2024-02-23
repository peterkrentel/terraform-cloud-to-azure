#How to setup terraform cloud for Azure:
https://learn.microsoft.com/en-us/azure/developer/terraform/overview
https://developer.hashicorp.com/terraform/tutorials/azure-get-started/azure-build

#How to migrate an existing state file:
https://developer.hashicorp.com/terraform/tutorials/azure-get-started/azure-remote 

Create service principal:
https://learn.microsoft.com/en-us/cli/azure/azure-cli-sp-tutorial-1?tabs=bash

az ad sp create-for-rbac --name <service_principal_name> --role Contributor --scopes /subscriptions/<subscription_id>

##Terraform Cloud Setup:
1. create the github repo
2. grant the github app for terraform cloud to your org/repo
3. once logged into terraform cloud
    - create project
    - create workspace
    - setup the workspace variables to allow connectivity to Azure Subscription via the service proncipal

4. add terraform code to your repo and those commits should trigger terraform cloud plan
5. then click apply

The purpose of this repo is purely for learning, and if need a windows vm, a quick way to spin one up.  The only manual part is granting "my local ip" access to the NSG at the moment.

The terraform is from an awesome tutorial for building things on azure:
https://www.youtube.com/watch?v=lH3KT9RUEOA&list=PLLc2nQDXYMHowSZ4Lkq2jnZ0gsJL3ArAw