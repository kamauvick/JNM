## JNM
A random trial on this awesome site.

> this is italics


# AZ Powershell commands

### 1. Deploy an azure vm running windows server 2016 Datacenter to an existing AVSet
- Create variables for all required parameters

>Azure vm **name** and **size**


    $vmName = "fishandchips"
    $vmSize = "Standard_DS2_V2"
   
    
>Target **resource group** and **location details**

    $resourceGroup = Get-AzResourceGroup -Name 'mySpecialRG'  #For an existing RG
    $location = $resourceGroup.Location   #Set location to the RG's location

>Target **Availability-set**,  **Virtual-Network,** and **Subnet**

    $availabilitySet = Get AzAvailabilitySet -ResourceGroupName $resourceGroup.ResourceGroupName
