# arm-templates

This repo contains ARM template samples for Azure Database for MySQL - Flexible Server

## Deploying the template

Deploy the templates from Azure Powershell using the below block of code.

```azurepowershell-interactive
$resourceGroupName = <sample-rg-name>
New-AzResourceGroupDeployment -ResourceGroupName $resourceGroupName `
    -TemplateFile "/Users/shreyaaithal/template/template.json" `
    -TemplateParameterFile "/Users/shreyaaithal/template/parameters.json"
```

Alternatively, deploy the templates from Azure CLI using the below block of code.

```azurecli-interactive
az deployment group create \
  --name mysql-deployment \
  --resource-group sample-rg-name \
  --template-file template.json \
  --parameters '@parameters.json'
```