# CompressPDF
### Made with ❤️ towards Privacy ⭐
- Works within your browser 🌐
- Data stays in your PC, Nothing is uploaded 📤❌
- No tracking & No ads 🚫
- Instant conversion ⚡
- Works best with Scanned Image PDFs 📷

## Deployment (Azure App Service Linux)

This project now deploys to Azure App Service (Linux) via GitHub Actions using OIDC.

### Workflow

- Workflow file: .github/workflows/azure-static-web-apps-victorious-river-0612d3f03.yml
- Trigger: push to master (and manual workflow_dispatch)
- Runtime: Node.js 20
- Deploy method: zip deploy via azure/webapps-deploy

### Required GitHub configuration

Repository variable:

- AZURE_WEBAPP_NAME: your Azure App Service name

Repository secrets:

- AZURE_CLIENT_ID: federated identity app registration client ID
- AZURE_TENANT_ID: Microsoft Entra tenant ID
- AZURE_SUBSCRIPTION_ID: Azure subscription ID

### Azure prerequisites

1. Create an Azure App Service (Linux, Node runtime).
2. Create an app registration/service principal for GitHub OIDC.
3. Add federated credential mapping for this repository and branch.
4. Assign least-privilege role on the App Service scope (or resource group).

After setup, a push to master deploys the current app.