# Azure PowerShell cheatsheet

## Start PowerShell on macOS
``pwsh``

## Install Az module
``Install-Module -Name Az -Force``

## Login to your Azure account
``Login-AzureRmAccount``

## List all Azure regions
``Get-AzLocation | select DisplayName, Location | Format-Table``

## List all Resource Groups
``Get-AzResourceGroup``

## List all Resources in a Resource Group
``Get-AzResource -ResourceGroupName yourRG | ft``

## Create a new Resource Group
``New-AzResourceGroup -Name ARMtest -Location "germanywestcentral"``

## Delete a Resource Group
``Remove-AzResourceGroup -Name dp200``

## Delete a Storage Account
``Remove-AzStorageAccount -ResourceGroupName "dp200" -AccountName "smdevarmfunctionsg"``

## Deploy an ARM template
```
$templateFile = "{provide-the-path-to-the-template-file}"

New-AzResourceGroupDeployment 
 -Name blanktemplate /`
 -ResourceGroupName ARMtest /`
 -TemplateFile $templateFile 
```
