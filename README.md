# Using VM-Series Firewalls and the Azure Application Gateway to Secure Internet-Facing Web Workloads
This ARM template deploys two VM-Series firewalls between a pair of Azure load balancers. The external load balancer is an Azure Application Gateway (a web load balancer) that also serves as the Internet facing gateway, which  receives traffic and distributes it to the VM-Series firewalls. The firewalls enforce security policies to protect your workloads, and send the allowed traffic to the internal load balancer which is an Azure Load Balancer (Layer 4) that load balances across a pair of sample Apache web servers. 


As demand for your web services increase, you can add more web servers and deploy additional VM-Series firewalls for more capacity. Each tier, the VM-Series firewalls and web servers, are deployed in separate Availability Sets for higher availability and redundancy against planned and unplanned outages. Refer to Azure documentation for more information on [Availability Sets] (https://docs.microsoft.com/en-us/azure/virtual-machines/virtual-machines-linux-manage-availability). A sample configuration file for VM-Series firewall is also included. After you import this configuration file, be sure to (a) customize the security policies to your needs and (b) <b>set a custom password</b> for the firewall instead of the value in the sample file. Refer to the documentation for steps on how to import the sample configuration file. 

**Support Policy**

***Supported***
 
This project is released under the official support policy of Palo Alto Networks through the support options that you've purchased, for example Premium Support, support teams, or ASC (Authorized Support Centers) partners and Premium Partner Support options. The support scope is restricted to troubleshooting for the stated/intended use cases and product versions specified in the project documentation and does not cover customization of the scripts or templates.
Only projects explicitly tagged with "Supported" information are officially supported. Unless explicitly tagged, all projects or work posted in our [GitHub repository] (https://github.com/PaloAltoNetworks) or sites other than our official [Downloads page] (https://support.paloaltonetworks.com/) are provided under the best effort policy.
 
**Documentation**
* Release Notes: Included in this repository.
* Technical Documentation:[VM-Series Deployment Guide] (https://www.paloaltonetworks.com/documentation/71/virtualization/virtualization/set-up-the-vm-series-firewall-in-azure/deploy-the-vm-series-and-azure-application-gateway-template.html)
* About the [VM-Series Firewall for Azure] (azure.paloaltonetworks.com)

[<img src="http://azuredeploy.net/deploybutton.png"/>](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FPaloAltoNetworks%2Fazure-applicationgateway%2Fmaster%2Fazuredeploy.json)