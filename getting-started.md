# Azure OpenAI + NLP using ChatGPT on SQL Engine

## Overall Estimated Duration: 4 Hours

## Overview

This application integrates Azure OpenAI's ChatGPT (GPT-4) with sophisticated data analytics to deliver comprehensive insights from a business database. It harnesses the power of AI to identify emerging trends, analyze customer behaviors, and predict future outcomes, equipping businesses with the tools they need to make strategic, data-driven decisions. By leveraging Azure App Services for reliable and scalable application hosting and Azure OpenAI for advanced natural language processing, this solution transforms complex data into actionable intelligence, offering deeper understanding and enhanced operational efficiency.

## Objective

In this lab, you will perform:

- **Open AI Setup and Installation of Application** : Learn to review and configure an OpenAI resource in Azure, followed by deploying an application to Azure App Service using the command-line interface. This exercise will cover setting up the resource, ensuring its proper integration, and successfully hosting the application in the cloud.
- **Quick Start With Hosted Demo Application** : Learn to interact with the hosted Demo Application, utilizing the Data Analysis Assistant and SQL Query Writing Assistant. This exercise focuses on analyzing data and leveraging AI tools to streamline data analysis and query generation.

## Pre-requisites
- **Fundamental Knowledge of Azure Services** : Knowing about some of the basic services like App Services.
- **Basic Understanding Programming Language** : basic understanding of programming languages like python or csharp.

## Architecture

In this hands-on lab, the workflow involves publishing a python or csharp webapplication to Azure App Services via the CLI, and integrating it with an OpenAI resource. The deployed web application uses the OpenAI resource to handle and respond to user requests.

## Architecture Diagram

## Getting Started with Lab

1. Once the environment is provisioned, a virtual machine (JumpVM) and lab guide will get loaded in your browser. Use this virtual machine throughout the workshop to perform the lab. You can see the number on the bottom of the lab guide to switch to different exercises of the lab guide.

   ![](images/getstartpage-01.png)
 
1. To get the lab environment details, you can select the **Environment Details** tab. Additionally, the credentials will also be emailed to your registered email address. You can also open the Lab Guide in a separate and full window by selecting the **Split Window** from the lower right corner. Also, you can start, stop and restart virtual machines from the **Resources** tab.

   ![](images/getstartpage-02.png "Enter Email")
 
   > You will see the SUFFIX value on the **Environment Details** tab, use it wherever you see SUFFIX or DeploymentID in lab steps.
 
## Login to Azure Portal

1. In the JumpVM, click on the Azure portal shortcut of the Microsoft Edge browser which is created on the desktop.

   ![](images/updated1.png)
   
1. On the **Sign in to Microsoft Azure** tab you will see the login screen, in that enter the following email/username, and click on **Next**. 

   * **Email/Username**: <inject key="AzureAdUserEmail"></inject>
   
      ![](images/signin-uname.png "Enter Email")
     
1. Now enter the following password and click on **Sign in**.
   
   * **Password**: <inject key="AzureAdUserPassword"></inject>
   
      ![](images/signin-pword.png "Enter Password")
     
1. If you see the pop-up **Stay Signed in?**, select **No**.

1. If you see the pop-up **You have free Azure Advisor recommendations!**, close the window to continue the lab.

1. If a **Welcome to Microsoft Azure** popup window appears, select **Maybe Later** to skip the tour.
   
1. Now you will see the Azure Portal Dashboard, click on **Resource groups** from the Navigate panel to see the resource groups.

   ![](images/select-rg.png "Resource groups")
   
1. Confirm that you have all resource groups present as shown below.

   ![](images/open-sql-rg.png "Resource groups")
   
1. Verify the resources deployed in the resource group.

   ![](images/resources.png "Resource groups")
   
1. Now, click on **Next** from the lower right corner to move on to the next page.

In this lab, you will review the Open AI deployments and review the code and publish it to Azure App Services. You will work with the hosted application and leverage AI tools to streamline data analysis and query generation

## Support Contact

The CloudLabs support team is available 24/7, 365 days a year, via email and live chat to ensure seamless assistance at any time. We offer dedicated support channels tailored specifically for both learners and instructors, ensuring that all your needs are promptly and efficiently addressed.

Learner Support Contacts:

- Email Support: labs-support@spektrasystems.com
- Live Chat Support: https://cloudlabs.ai/labs-support

## Happy Learning!!
