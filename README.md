# Qlik Talend Cloud Documentation Generator

### Introduction

This is a Qlik Application Automation that has been built to automatically generate the documentation of one or more Data Integration Projects built with [Qlik Talend Cloud](https://help.qlik.com/en-US/cloud-services/Subsystems/Hub/Content/Sense_Hub/DataIntegration/Introduction/Data-services.htm). The idea is to fire the automation and select the Project(s) to be documented and the way the user wants to receive the final output: via email or an HTML file saved in a Cloud Storage.

### Installation

1. Download the JSON file provided in this repository
2. Go to your Qlik Cloud tenant and [create a new Qlik Application Automation](https://help.qlik.com/en-US/cloud-services/Subsystems/Hub/Content/Sense_QlikAutomation/introduction/creating-automation.htm)
3. Select the Blank Template and give it a name and - optionally - a description
4. Once you're in the canvas, right-click on the it and select [Upload Workspace](https://help.qlik.com/en-US/cloud-services/Subsystems/Hub/Content/Sense_QlikAutomation/introduction/navigating-UI.htm)
5. Select the JSON you just downloaded and import it: the automation should appear in your canvas
6. Now you need to click on the **"Variable - vBearerToken"** block and add your Qlik Cloud API ([read here on how to create your API Key](https://help.qlik.com/en-US/cloud-services/Subsystems/Hub/Content/Sense_Hub/Admin/mc-generate-api-keys.htm))
7. If you intend to use the Cloud Storage option, please move towards the top of the canvas to insert the name of your S3 Bucket in the **"Variable - vStorageBucket"** block
8. If you want to use your own Company Logo, please click on the **"Variable - vCompanyLogo"** block and paste the Base64 text of the converted image
9. Move towards the bottom of the canvas and locate the MS O365 block: click on it and [setup your O365 connection](https://help.qlik.com/en-US/cloud-services/Subsystems/Hub/Content/Sense_QlikAutomation/connector-blocks/connectors-list.htm)
10. If you intend to use the Cloud Storage option, please setup the connection to your own Cloud Storage in the corresponding blocks (by default they're setup for AWS S3)
12. You're ready to go: click on "Run" to execute the automation

## Known Issues

Some projects may not have all parts cataloged, therefore some information may be missing from the resulting documentation. This is not due to the automation, but to the way the assets are cataloged in Qlik Talend Cloud.

# Authors & Credits

This automation has been created by [Alberto Vaghi](mailto:cii@qlik.com) with the magic support by [Giacomo Brioschi](mailto:fqy@qlik.com).
