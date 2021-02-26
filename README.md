# On an existing Web App, Bind a custom domain, create the DNS record to validate, Create a Managed Certificate (Free) and Bind it

[![Deploy To Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fcoelho5br%2Fwebapp-bind-name-and-managed-certificate%2Fmaster%2Fcustomdomain.json)
[![Visualize](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/visualizebutton.svg?sanitize=true)](http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Fcoelho5br%2Fwebapp-bind-name-and-managed-certificate%2Fmaster%2Fcustomdomain.json)


To deploy this template, you need to have the following resources:

1. Existing Web App
2. Domain purchased and the DNS zone is hosted in azure. DNS zone does not need to be on the same resource Group
3. The App Service Plan (serverFarm) resource name.


This arm deployment will:

1. Createa a DNS record with ASUID, CNAME or A when the DNS zone is on a different resource Group
2. Add a Custom Domain to the Web App.
3. Create a  Managed Certificate (Free).
4. Bind the Managed Certificate to the app. It can also deploy a APEX/naked domain.