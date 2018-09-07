# Data Factory Orchestration

This demo how to use Logic Apps to orchestrate multiple Data Factory Pipelines.

The Logic Apps relies on a hierarchy of pipelines (parent-children) stored in a SQL Database.

[![Deploy button](http://azuredeploy.net/deploybutton.png)](https://portal.azure.com/#create/Microsoft.Template/uri/https:%2F%2Fraw.githubusercontent.com%2Fvplauzon%2Flogic-apps%2Fmaster%2Fdata-factory-orchestration%2FDeployment%2Fdeploy.json)

```PowerShell
Get-AzureRmLogicAppTriggerCallbackUrl -ResourceGroupName <Resource Group Name> -Name pipeline -TriggerName manual
```