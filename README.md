How to setup terraform cloud for Azure:
https://learn.microsoft.com/en-us/azure/developer/terraform/overview
https://developer.hashicorp.com/terraform/tutorials/azure-get-started/azure-build

How to migrate an existing state file:
https://developer.hashicorp.com/terraform/tutorials/azure-get-started/azure-remote 

az ad sp create-for-rbac --name <service_principal_name> --role Contributor --scopes /subscriptions/<subscription_id>

Terraform Cloud Setup:
1) create the github repo
2) grant the github app for terraform cloud to your org/repo
3) once logged into terraform cloud
    a) create project
    b) create workspace
    c) setup the workspace variables to allow connectivity to Azure Subscription via the service proncipal

4) add terraform code to your repo and those commits should trigger terraform cloud plan
5) then click apply