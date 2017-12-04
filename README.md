# powershell_azure_vm
Set up an Azure VM via PowerShell

```
# sudo command for PowerShell (makes it a lot easier ;) )
Set-ExecutionPolicy -ExecutionPolicy Unrestricted

# Install the Azure Resource Manager modules from the PowerShell Gallery (it will ask you for permission twice)
Install-Module AzureRM -AllowClobber

# Imports the PowerShell Azure Module 
Import-Module AzureRM

#glimpse of all Azure commands in PowerShell
Get-Command *azure*

#Log in to your Azure Account (it will open up a Login window)
Add-AzureRmAccount 
```
![Loginwindow](https://fhwnspeicher.blob.core.windows.net/eins/PS_azure_login.png)  
```
#take a look at your Azure VMs
Get-AzureRmVM

#create a new VM on Azure
New-AzureRmVM [-ResourceGroupName] <string> [-Location] <string> [-VM] <PSVirtualMachine> [[-Zone] <string[]>]  [<CommonParameters>]

#start your VM
Start-AzureRmVM [-ResourceGroupName] <string> [-Name] <string>  [<CommonParameters>]

#stop your VM
Stop-AzureRmVM [-ResourceGroupName] <string> [-Name] <string>  [<CommonParameters>]

#remove your VM
Remove-AzureRmVM [-ResourceGroupName] <string> [-Name] <string>  [<CommonParameters>]
```
