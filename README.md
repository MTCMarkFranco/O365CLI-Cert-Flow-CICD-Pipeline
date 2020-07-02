# O365CLI-Cert-SPFX-CICD-Pipeline
A basic YAML pipeline to build, upload and deploy a SharePoint Framework Project (*.sppkg) file to Microsoft 365.

Please follow the steps detailed in this article before using the pipeline in this project. You need to replace the following variable values:
- OFFICE365CLI_AADAPPID
- OFFICE365CLI_TENANT
- o365_app_catalog_site_url
- cert_thumbprint
- spfx-pkg

There is a sample SharePoint Framework  package file provided that can be used as is for your testing. This SPPKG enables you to add Azure Application Insights to your SPO site.

## Optional steps:
If you are interested in actually using the Azure App Insights and configure it with your own instrumentation key, then please follow below steps:
- To add custom action to a specific site:
1. The GUID (0d62cd95...) is the client side component id from the SPFx project. Do not change it.
2. Update the SPO site url
3. Replace the appInsightsKey GUID (with your instrumentation key)

> spo customaction add -c 0d62cd95-51fa-4307-b7da-0ebcf03c0a9d -s Site -t "AzureAppInsights" -n "AzureAppInsights" -l "ClientSideExtension.ApplicationCustomizer" --verbose -u https://YOURTENANT.sharepoint.com/sites/SITENAME -p '{"appInsightsKey":"4bc670b6-2b3a-491d-9984-4123dad1201b"}'
 
- To list all the custom actions (spfx app customizer extensions) for the SPO site
>spo customaction list -u https://YOURTENANT.sharepoint.com/sites/SITENAME 

- To remove the custom action, use the GUID from the output of the above command in below command.
>spo customaction remove -i 1d7cc2d2-9ef4-40b5-838d-7135e02b2633 -u https://YOURTENANT.sharepoint.com/sites/SITENAME
