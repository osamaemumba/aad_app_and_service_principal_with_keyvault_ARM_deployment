### NOT WORKING AS REQUIRED RIGHT NOW

- The button deployment aims to create a service principal through deployment script using user azure Id and password.
- The deployment script is also given user assigned managed identity. And this identity is given contributor role on current resource group.
- The key vault access policy is also set to give 'get and list secrets' permissions to the user assigned managed identity.
- The password is stored into the keyvault (being deployed) and then it should be retrieved into the deployment script, but it gives the keyVault access denied error.


- The file 'azuredeploy_single_without_keyvault.json' is a single file to create ad app and service principal.
- #### This file only works when the user password is hardcoded into the script. i.e. it doesnot work when parameterized, whether of type string or secureString.

[![Deploy To Azure](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.svg?sanitize=true)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fosamaemumba%2Fpurview-poc%2Fmain%2Fazuredeploy.json)