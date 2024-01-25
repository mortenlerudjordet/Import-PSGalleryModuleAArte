# Import-PSGalleryModuleAArte

This Azure Automation Runbook imports a module and all of it's dependencies into Azure Automation Runtime Environment from PowerShell Gallery.
This is meant to only run from an Automation account with Runtime Environment activated.

Can choose to use this Runbook to import the Az-module instead of the RTE default way.
If so, make sure to first import Az.Accounts, Az.Automation and Az.Resources through the portal.

To import into different runtime environments with this Runbook, either change the RTE link, or create multiple Runbooks with different names.
If doing the later, remember to update the $RunbookName parameter in the Runbook to match the new name, as this is used to dynamically find the name of the RTE the Runbook is linked to.

NOTE:
    System-generated RTEs can not be updated by this Runbook directly.
