# Data Factory Orchestration

This demo how to use Logic Apps to orchestrate multiple Data Factory Pipelines.

The Logic Apps relies on a hierarchy of pipelines (parent-children) stored in a SQL Database.

It can be deploy now:

[![Deploy button](http://azuredeploy.net/deploybutton.png)](https://portal.azure.com/#create/Microsoft.Template/uri/https:%2F%2Fraw.githubusercontent.com%2Fvplauzon%2Flogic-apps%2Fmaster%2Fdata-factory-orchestration%2FDeployment%2Fdeploy.json)

There are a few steps to follow afterwards:

* Get the Callback URL for the Logic App with the following PowerShell command:
```PowerShell
(Get-AzureRmLogicAppTriggerCallbackUrl -ResourceGroupName <Resource Group Name> -Name pipeline -TriggerName manual).Value
```
* Re-run the ARM template using that value as the *Logic App Call Back* parameter
* Populate the data factory with pipelines
* Create a table *dbo.Pipeline* in the *meta* database
```sql
CREATE TABLE [dbo].[Pipeline] (
    [PipelineName]       VARCHAR (32) NOT NULL,
    [ParentPipelineName] VARCHAR (32) NULL
);
```
* Populate that table with a hierarchy of pipelines corresponding to the pipelines names created in data factory
* Authenticate the *df-connection-region* connection