# SEPPmail Load-balancing Cluster

This ARM-Template lets you deploy a 2-node SEPPmail cluster, including a pre-configured
Azure Network Load Balancer. The virtual machines are created with the SEPPmail Marketplace VM images.

As of today (early October 2019) we use the 'smvm11' image which represents SEPPmail Version 11.0.5.
Please see the schema graphic for a representation of the technical schema.
![NLB Cluster Schema] (https://github.com/seppmail/AzureNLBCluster/SEPPmailLbCluster.png)

## Files

### SEPPmailLbCluster.json

This is the ARM-Template deploying the resources into your Azure Subscription. It should work without any parameters, because we have set default values in every parameter.

After a successful setup, the template will provide access details to the WebInterface, GINA and SMTP ports of the cluster. See output-section of the template for details.

### SEPPmailLbClusterParameters.json

ARM-Template parameter file. Use this file to change names, IP-Ranges and other parameters used in the template.

### deploy.ps1

Example deployment script in Powershell. You could use Az-CLI as well, it would produce the same results.
This example creates a resource group and deploys all resources in this group. If you want to change the deployment location or the resource group name, change it to your needs.
