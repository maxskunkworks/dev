# Office 365 Update Notification (v0.1)

**Time to deploy**: 2 minutes

The **Office 365 Update Notification** template provisions a logic app and function app that notifies a specified email address when updates to the Office 365 endpoints are published.

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmaxskunkworks%2Fdev%2Fmaster%2FO365-Endpoints-Notifications%2Fazuredeploy.json" target="_blank">
<img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Fmaxskunkworks%2Fdev%2Fmaster%2FO365-Endpoints-Notifications%2Fazuredeploy.json" target="_blank">
<img src="http://armviz.io/visualizebutton.png"/>
</a>

## Usage

Click the "Deploy to Azure" button to open the deployment UI in the Azure portal.

## Solution overview and deployed resources

The following resources are deployed as part of the solution:

+ **Logic App**: Windows Server 2012 R2 or 2016 VM configured as a domain controller and DNS with static private IP address
+ **Function App**: Windows Server 2012 R2 or 2016 VM(s) joined to the domain. IIS is installed, and C:\Files containing example.txt is shared as "Files". App servers are deployed with a second NIC connecting to the backend subnet.

## Solution notes

## Known issues

`Tags: Office 365 endpoints`
___
Developed by the **MAX Skunkworks Lab**  
Author: Kelley Vice (kvice@microsoft.com)  
https://github.com/maxskunkworks

![alt text](images/maxskunkworkslogo-small.jpg "MAX Skunkworks")

Last update: _4/16/2019_

## Changelog

+ **4/16/2019**: Original commit