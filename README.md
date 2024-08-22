# opinionated-swa-template

The repo contains an opinionated template for creating an Azure Static Web App (SWA) with a managed Azure Function API.

## Applying the Template

Start by making a GitHub repo out of this template. This is done by using a GitHub feature:

Go to GitHub and do X Y and Z. (_Details to follow._)

### One-time Configuration

In order for GitHub Actions to deploy to your Azure SWA you need to give it some permissions by deciding where you will deploy your SWA and setting up a couple of secrets so GitHub has needed permissions.

az login

az staticwebapp secrets list --name <your-static-web-app-name> --query "properties.apiKey" -o tsv
az staticwebapp secrets list --name <Your_Static_Web_App_Name> --resource-group <Your_Resource_Group_Name>
az staticwebapp secrets regenerate --name <Your_Static_Web_App_Name> --resource-group <Your_Resource_Group_Name>

gh auth login

gh secret set AZURE_STATIC_WEB_APPS_API_TOKEN_ICY_COAST_0A861511E --body <Your_Azure_Static_Web_Apps_API_Token>

xxgh secret set AZURE_STATIC_WEB_APPS_API_TOKEN_ICY_COAST_0A861511E --body "<deployment-token-value>"

xxgh secret set AZURE_STATIC_WEB_APPS_API_TOKEN_ICY_COAST_0A861511E <your_azure_token>
xxgh secret set GITHUB_TOKEN <your_github_token>

gh secret list

The GITHUB_TOKEN is automatically generated by GitHub Actions and is available by default in your workflow. There’s no need to generate this manually.

## Using the Template

Once you have made your own GitHub repo from this template, you are ready to go.

### Updating to Match Your Needs

The front-end website is vanilla HTML, CSS, and JavaScript. This is a starting point. You will update to match your own needs.

The back-end API is C# on .NET. This is a starting point. You will update to match your own needs.

### Local Deployment

The ```swa``` CLI can be used to run, test, and debug locally.

### Deployment to Production

Code lives in GitHub. There is a GitHub Action workflow configured to automatically deploy to Production environment in Azure when any updates are checked into main branch.

### Deployment to Lower Environments

The ```swa``` CLI can be used to deploy to lower (non-production) environments like Dev.
