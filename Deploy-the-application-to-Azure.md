# SQL-ChatGPT-Workshops

## Overview

This application demonstrates the of Open AI (ChatGPT/GPT-4) to help answer business questions by performing advanced data analytic tasks on a business database. Examples of questions are:

 * Simple: Show me daily revenue trends in 2016 per region
 * More difficult: Is that true that top 20% customers generate 80% revenue in 2016?
 * Advanced: Forecast monthly revenue for next 12 months starting from June-2018

The application supports Python's built-in SQLITE as well as your own Microsoft SQL Server.

## Exercise 1: Open AI setup and Installation of Application

In this exercise, you will be setting up the Open AI resource and installtion of application locally.

### Task 1: Create Open AI resource

1. In the Azure portal, search for **Azure OpenAI** **(1)** in the top search box then select **Azure OpenAI** **(2)** under services.

   ![](images/search-openai.png "Azure OpenAI")
   
1. From the **Cognitive Services | Azure OpenAI** pane, click on **Create**.

   ![](images/select-openai.png "Azure OpenAI")
   
1. In the Create Azure OpenAI pane under Basics tab, select the default subscription and select the existing **sql-chat-gpt-<inject key="Deployment ID" enableCopy="false"/>** resource group. Select **East US** as Region, enter Name as **SQL-OpenAI-<inject key="Deployment ID" enableCopy="false"/>** and select **Standard S0** for Pricing tier. Click on **Next**

   ![](images/create-openai-basics.png "Azure OpenAI")
   
1. Leave default settings for Network and Tags tabs, click on **Next**.

1. In the Review + submit pane, verify that validation passed and then click on **Create**.

   ![](images/create-openai-validate.png "Azure OpenAI")
   
1. Deployment will take 5 minutes to complete. Once the deployments is succeeded, click on **Go to resource**.

   ![](images/gotoresource.png "Azure OpenAI")
   
1. In the Azure OpenAI resource pane, click on **Go to Azure OpenAI Studio** it will navaigate to **Azure AI Studio**.

   ![](images/azureaIstudio.png "Azure OpenAI")
   
1. In the **Azure AI Studio**, select **Deployments (1)** under Management and click on **+ Create new deployment (2)**    
   
   ![](images/azureaIstudiodep.png "Azure OpenAI")
   
1.  On the Deploy model pop-up, from the drop-down select **gpt-35-turbo (1)** for Select a Model, then select the Modle version **0301 (2)**, enter deployment name as **sql-chatgpt-model (3)** then click on **Save (4)**. Copy OpenAI Model name into the text file for later use.
  
      ![](images/openai-create.png "Azure OpenAI")

1. Naviagte back to [Azure portal](http://portal.azure.com/), search and select **Azure OpenAI**, from the **Cognitive Services | Azure OpenAI pane**, select the **SQL-OpenAI-<inject key="Deployment ID" enableCopy="false"/>**.

1. Now select **Keys and Endpoints** **(1)** under Resource Management and click on **Show Keys** **(2)**. Copy the **KEY 1** **(3)** and **Endpoint** **(4)**, store it in a text file for later use.

   ![](images/openai-keys-ep.png "Azure OpenAI")
      
### Task 2: Deploy the application to Azure

1. In the LabVM, open **File Explorer** naviagte to the `C:\LabFiles\OpenAIWorkshop-Automation\infra` **(1)** path, right click on **main.bicep (2)**, and select **Open with Code (3)**.

   ![](images/file-select.png "Azure OpenAI")

2. In **main.bicep** file edit the line number **22** by replacing the **actualrgname** with **sql-chat-gpt-<inject key="Deployment ID" enableCopy="false"/>** and save the file by clicking on **Ctrl + S**  

      ![](images/file-update.png "Azure OpenAI")

3. In the LabVM, navigate to Desktop and search for `cmd` in the search box then click on **Command Prompt**.

4. Run the below command to change the directory.

   ```bash
   cd C:\LabFiles\OpenAIWorkshop-Automation
   ```

5. Run the below command to **Authenticate with Azure**. It will redirect to Azure authorize website, select your account.

   ```bash
   azd auth login
   ```

6. Run the below command to **Create a new environment** and replace `{DeploymentId}` with **<inject key="Deployment ID" enableCopy="false"/>**.

   ```bash
   azd env new sql-chat-gpt-{DeploymentId}
   ```

7. Run the below command to Provision Azure resources, and deploy your project with a single command.

   ```bash
   azd up
   ```

8. Please select your Azure Subscription to use, enter `1` and click on **Enter** button.

9. Please select an Azure location to use, select the location same as **Resource Group** location, and click on **Enter** button. You can change the location using up and down arrow.

10. Once the deployment succeeds you will should see the following message **SUCCESS: Your application was provisioned and deployed to Azure**. The deployment might take above 5 minutes .

      ![](images/app-deployment-output.png "Azure OpenAI")

11. Once the Deploymet got succedded naviagte back to the Azure portal, search and select **App service**, select the available web app which you have deployed in the previous step.

12. Next, click on **Browse** to open your Web application.

      ![](images/webapp.png "Azure OpenAI")
      
      ![](images/webapp1.png "Azure OpenAI")

## Summary

In this exercise, you have completed OpenAI Setup and hosting a demo application locally. You will be exploring the demo application in the next exercise, click **Next** to continue with the lab.
   
