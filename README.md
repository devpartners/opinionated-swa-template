# opinionated-swa-template

The repo contains an opinionated template for creating an Azure Static Web App (SWA) with a managed Azure Function API.

## Applying the Template

Start by making a GitHub repo out of this template. This is done by using a GitHub feature:

Go to GitHub and do X Y and Z.

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
