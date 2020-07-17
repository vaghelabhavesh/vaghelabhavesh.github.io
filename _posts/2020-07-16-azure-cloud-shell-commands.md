---
layout: post
comments: true
title: "Azure Cloud Shell Commands"
categories: blog
author:
- Bhavesh Vaghela
meta: "Springfield"
---

### What is Azure Cloud Shell?
Azure cloud shell is a command line tool which can be used for managing azure resources from command line. It is accessible from browser and it is interactive.

**How to launch the Azure Cloud Shell?**
There are two ways to launch the Azure Cloud Shell in browser.

First option is to go to [Azure Portal](https://portal.azure.com/) and click the cloud shell icon in top navigation bar.

![Azure Portal](/images/2020-07-16/1.Portal.png)

Second option is to go to [shell.azure.com](https://shell.azure.com/) and click on the Launch Cloud Shell button.

![Azure Shell](/images/2020-07-16/2.Shell.png)

Now lets talk about some cloud shell command which you can execute in this cloud shell.

- **List the regions that are available from your Azure subscription:**
To List the regions that are available from your Azure subscription, try the following az account command in azure shell.

      az account list-locations \
        --query "[].{Name: name, DisplayName: displayName}" \
        --output table

     ![List Regions](/images/2020-07-16/3.ListRegion.png)

 - **Set the default region:**
To set the default region, try the following az configure command in azure shell and provide the name of the region that you want to set as default.

      **`az configure --defaults location=westindia`**

     ![Set Default](/images/2020-07-16/4.SetDefault.png)
 
 - **Create a resource group:**
To create a resource group, try the following az group create command in azure shell and specify the name of the resource that you want to create.

      **`az group create --name tailspin-space-game-rg`**

     ![Create Resource](/images/2020-07-16/5.CreateResource.png)

- **Create App Service plan:**
To create the app service plan, try the following az appservice plan create command in azure shell and provide the resource group name that you created above and specify plan name that you want to create.

      az appservice plan create \
        --name tailspin-space-game-asp \
        --resource-group tailspin-space-game-rg \
        --sku B1

     ![Create App Service Plan](/images/2020-07-16/6.CreateAppServicePlan.png)

- **Create App Service:**
To create the web app, try the following az webapp create command in azure shell and provide the resource group name, plane name and specify the app service name that you want to create.

      az webapp create \
        --name tailspin-space-game-web-dev-$webappsuffix \
        --resource-group tailspin-space-game-rg \
        --plan tailspin-space-game-asp

     ![Create App Service](/images/2020-07-16/7.CreateAppService.png)

- **List App Services:**
To list the host name and state of App Service instance, try the following az webapp list command in azure shell.

      az webapp list \
        --resource-group tailspin-space-game-rg \
        --query "[].{hostName: defaultHostName, state: state}" \
        --output table

     ![List App Services](/images/2020-07-16/8.ListAppServices.png)

 - **Delete a resource group:**
To delete a resource group, try the following az group delete command in azure shell and provide the name of the resource that you want to delete.

      **`az group delete --name tailspin-space-game-rg`**

     ![Delete Resource](/images/2020-07-16/9.DeleteResource.png)

### Wrap up
These were some basic commands that can get you started with Azure using cloud shell if you prefer the command line tool over GUI.

Happy Coding.
