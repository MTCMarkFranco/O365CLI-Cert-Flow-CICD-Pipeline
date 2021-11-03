# O365CLI-Cert-Flow-CICD-Pipeline
A basic YAML pipeline to Enable a Power Automate Flow via Azure Devops Pipeline

Please follow the steps detailed in this article before using the pipeline in this project. You need to replace the following variable values:
- OFFICE365CLI_AADAPPID
- OFFICE365CLI_TENANT
- cert_thumbprint


- To Enable a Power Automate Flow
>o365 flow enable --environment "MS Personal Productivity (msdefault)" --name "Power Apps button" --asAdmin

- Walkthrough on how to implement this is here:
>https://techcommunity.microsoft.com/t5/core-infrastructure-and-security/using-azure-ad-app-and-certificate-with-office-365-cli-in-azure/ba-p/1539553