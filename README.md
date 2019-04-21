# sophos-cloud-optix
Deployment template to deploy sample resources to Azure to test the functionality of Sophos Cloud Optix. 

Deploying
=========
1) Press the deployment button and enter your Azure credentials when prompted.

[![Deploy to Azure](https://azuredeploy.net/deploybutton.png)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fdavidokeyode%2Fsophos-cloud-optix%2Fmaster%2Fcloud-optix-demo.json)

Template Information
====================
The template deploys the following resources:

**a) Virtual Network**
* **Frontend** - _FESubnet / 10.0.1.0/24_
* **Application** - _AppSubnet / 10.0.2.0/24_
* **Database** - _DBSubnet / 10.0.3.0/24_

It also creates three Network Security Groups - one per subnet:
* **Frontend** - _FE_NSG_
* **Application** - _App_NSG_
* **Database** - _DB_NSG_

Each NSG is then associated with a subnet:
* _FESubnet_ to _FE_NSG_
* _AppSubnet_ to _App_NSG_
* _DBSubnet_ to _DB_NSG_

**b) Virtual Machines**
* **Web Server** - _Ubuntu Linux_
* **Application Server** - _Ubuntu Linux_
* **Database Server** - _Ubuntu Linux running MongoDB_

**c) Azure Storage Account**
* **Azure Storage account with three blob containers**

**d) Azure SQL**
* **Azure SQL Server with a database instance**

Useful Links
============
* [Sohos Cloud Optix URL](https://www.sophos.com/en-us/products/cloud-optix.aspx)
* [Sohos Cloud Optix FAQ](https://community.sophos.com/kb/en-us/133806)
* [Authoring Azure Resource Manager templates](https://azure.microsoft.com/en-us/documentation/articles/resource-group-authoring-templates/)
