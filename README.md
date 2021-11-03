# O365CLI-Cert-Flow-CICD-Pipeline
A basic YAML pipeline to build, upload and deploy a SharePoint Framework Project (*.sppkg) file to Microsoft 365.

Please follow the steps detailed in this article before using the pipeline in this project. You need to replace the following variable values:
- OFFICE365CLI_AADAPPID
- OFFICE365CLI_TENANT
- cert_thumbprint


- To Enable a Power Automate Flow
>o365 flow enable --environment "MS Personal Productivity (msdefault)" --name "Power Apps button" --asAdmin

