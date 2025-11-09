# github-actions-dotnet

For the CI/CD pipeline you need to have a azure managed identity to be able to deploy this Web App to Azure App Services

This managed identiy needs to have federated creadentails for GitHub Actions setup

On the Azure App Service a role assignment for the managed identity has to be set