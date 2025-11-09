# github-actions-dotnet

---

## Prerequisites

### GitHub Actions

You need to have two environments configured: dev, prod

Both environments need to have some secrets set: 
- AZURE_CLIENT_ID -> to fetch this you need to have a managed identiy setup (described in the Azure section)
- AZURE_SUBSCRIPTION_ID
- AZURE_TENANT_ID

---

### Azure 

Required resources: resource group, app service, managed identity both for dev and prod

Note: the dev and prod environment are in the same subscription, which is not best practice!


For the CI/CD pipeline you need the Azure Managed Identity to be able to deploy the web app to Azure App Services

This managed identiy needs to have federated creadentails for GitHub Actions (choose the environment as the Entity: dev/prod)

On the Azure App Service a role assignment for the managed identity has to be set