# Create_Azure Managed disk_ARM template


Task: Create an Azure managed disk by using an ARM template

In the Azure portal, search for and select Deploy a custom template.

On the Custom deployment blade, click Build your own template in the editor.

On the Edit template blade, click Load file and upload the template.json file you downloaded in the previous task.

Within the editor pane, remove the following lines:

"sourceResourceId": {
    "type": "String"
},
"hyperVGeneration": {
    "defaultValue": "V1",
    "type": "String"
},      
Note: These parameters are removed since they are not applicable to the current deployment. In particular, sourceResourceId, sourceUri, osType, and hyperVGeneration parameters are applicable to creating an Azure disk from an existing VHD file.

Save the changes.

Back on the Custom deployment blade, click Edit parameters.

On the Edit parameters blade, click Load file and upload the parameters.json file you downloaded in the previous task, and Save the changes.

Back on the Custom deployment blade, specify the following settings:

Setting	Value:-

**Subscription the name of the Azure subscription you are using in this lab

Resource Group	the name of a new resource group az104-03b-rg1

Region	the name of any Azure region available in the subscription you are using in this lab

Disk Name	az104-03b-disk1

Location the value of the location parameter you noted in the previous task

Sku	Standard_LRS

Disk Size Gb	32

Create Option	empty

Disk Encryption Set Type	EncryptionAtRestWithPlatformKey

Network Access Policy	AllowAll

Select Review + Create and then select Create.

Verify that the deployment completed successfully.


**Delete the resources**
