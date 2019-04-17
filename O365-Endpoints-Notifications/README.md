# Office 365 Update Notification (v0.2)

**Time to deploy**: 2 minutes

The **Office 365 Update Notification** template provisions an Azure Logic app that notifies the specified Office 365 email address when updates to the Office 365 endpoints are published, and an App Service Function app that converts the JSON output of endpoint updates to human-readable tables.

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmaxskunkworks%2Fdev%2Fmaster%2FO365-Endpoints-Notifications%2Fazuredeploy.json" target="_blank">
<img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Fmaxskunkworks%2Fdev%2Fmaster%2FO365-Endpoints-Notifications%2Fazuredeploy.json" target="_blank">
<img src="http://armviz.io/visualizebutton.png"/>
</a>

**NOTE**: You must specify an Office 365 email account for the solution to work.

## Usage

Click the "Deploy to Azure" button to open the deployment UI in the Azure portal.

## Solution overview and deployed resources

The following resources are deployed as part of the solution:

+ **Logic app**: Triggered by the Office 365 Endpoints RSS feed, the LOgic App notifies the specified email address when updates to the Office 365 endpoints are published.
+ **App Service**: The App Service Function app converts the JSON output of endpoint updates to human-readable tables and add them to the email notification.
+ **App Service Plan**: Web services to support the App Service.
+ **App Insights**: Provides monitoring and logging for solution components.
+ **API Connections**: Connects the solution to an Office 365 email account and the RSS feed.
+ **Storage account**: Storage for log files and usage/dignostics data.

## Solution notes

+ You can modify the Logic app with additional functionality, such as adding an approval process or additional outputs targeted for your organization's particular workflow for updating Office 365 endpoints.
+ See [Creating a Microsoft Flow to email yourself when an Office 365 IP/URL change occurs](https://github.com/pandrew1/Office365-IPURL-Samples/tree/master/FlowNotifications) for additional solution details and procedures for manually building the solution.

## Known issues

`Tags: Office 365 endpoints`
___
Developed by the **MAX Skunkworks Lab**  
Authors:

+ Kelley Vice (kvice@microsoft.com)
+ Paul Andrew (pandrew@microsoft.com)

https://github.com/maxskunkworks

![alt text](https://raw.githubusercontent.com/oualabadmins/lab_deploy/master/common/images/maxskunkworkslogo-small.jpg "MAX Skunkworks")

Last update: _4/17/2019_

## Changelog

+ **4/16/2019**: Original commit
+ **4/17/2019**: Updated function build zip file