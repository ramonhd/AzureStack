# Azure Stack
This is an example template for deploying VM-Series (BYOL edition, PAN-OS 8.1 or higher) on your Azure Stack deployments. The template creates a VM-Series VM with 3 NICs that should be connectd to your management, untrust and trust subnets in a VNET. 

Note: VM-Series will not be directly visible in the Azure Stack Marketplace via syndication since the image (VHD) for it is normally hidden behind a Solution Template in the public Azure Marketplace. The Azure Stack administrator will need to syndicate VM-Series using the [steps described here](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-download-azure-marketplace-item). Next you can use template below or other [methods](https://github.com/Azure/AzureStack-QuickStart-Templates/tree/master/101-vm-linux-create) to  deploy it. For other example templates from Microsoft [see here](https://docs.microsoft.com/en-us/azure/azure-stack/user/azure-stack-create-vm-template).

## Deployment steps
* Login to your AzureStack portal
* From left-side panel, search/select Templates > Create a new template
* Copy-paste the contents of the template provided here
* Deploy it and provided necessary parameters.

Detailed deployment steps can be [found here](https://www.paloaltonetworks.com/documentation/81/virtualization/virtualization/set-up-the-vm-series-firewall-on-azure/deploy-the-vm-series-firewalls-on-azure-stack). 
  
You can deploy the VM-Series using your own custom templates (or PowerShell for Azure Stack) by using the following variables to refer to the VM-Series image:
```
Publisher: paloaltonetworks
Offer: vmseries1
SKU: byol
Version: 8.1 (or latest)
````

## Support: Community Supported
Unless otherwise noted, these templates are released under an as-is, best effort, support policy. These scripts should be seen as community supported and Palo Alto Networks will contribute our expertise as and when possible. We do not provide technical support or help in using or troubleshooting the components of the project through our normal support options such as Palo Alto Networks support teams, or ASC (Authorized Support Centers) partners and backline support options. The underlying product used (the VM-Series firewall) by the scripts or templates are still supported, but the support is only for the product functionality and not for help in deploying or using the template or script itself. Unless explicitly tagged, all projects or work posted in our GitHub repository (at https://github.com/PaloAltoNetworks) or sites other than our official Downloads page on https://support.paloaltonetworks.com are provided under a community supported, best effort, policy.
