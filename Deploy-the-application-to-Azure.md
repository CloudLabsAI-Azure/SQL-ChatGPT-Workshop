# Exercise 1: Open AI Setup and Installation of Application

### Estimated Duration : 1 Hour

In this exercise, you will be setting up the Open AI resource and installation of the application to Azure.

## Objectives

In this Exercise, you will complete the following tasks:
- Task 1: Review Open AI resource
- Task 2: Deploy the application to Azure

## Task 1: Review Open AI resource

In this task, you will be reviewing the Open AI deployments.

1. In the Azure portal, search for **Azure OpenAI** in the top search box then select **Azure OpenAI** under services.

   ![](images/search_openai.png "Azure OpenAI")
   
1. From the **Azure AI Services | Azure OpenAI** pane, select **SQL-OpenAI-<inject key="Deployment ID" enableCopy="false"/>**.

   ![](images/sql_openai1.png)
   
1. In the Azure OpenAI resource pane, click on **Go to Azure AI Foundry portal** it will navigate to **Azure AI Foundry portal**.

   ![](images/im1.png "Azure OpenAI")
      
1. In the **Azure AI Foundry**, select **Deployments** under Shared resources and verify that **gpt-35-turbo** model is present with the deployment name as **sql-chatgpt-model**, review that the capacity of the model is set to **15K TPM**. Copy the OpenAI Model name into the text file for later use.
   
   ![](images/im2.png "Azure OpenAI")

   > **Note**: Click on the **Expand** button, if you dont see the left side navigation pane.

   ![](images/im3.png "Keys and Endpoints")          
   
1. Naviagte back to [Azure portal](http://portal.azure.com/), search and select **Azure OpenAI**, from the **Azure AI Services | Azure OpenAI pane**, select the **SQL-OpenAI-<inject key="Deployment ID" enableCopy="false"/>**.

1. Now select **Keys and Endpoints** **(1)** under Resource Management and click on **Show Keys** **(2)**. Copy the **KEY 1** **(3)** and **Endpoint** **(4)**, and store them in a text file for later use.

   ![](images/keys-1.png)

   > **Note**: If you dont see the Left side Navigation pane, click on the three horizontal line on the top left corner.

      
## Task 2: Deploy the application to Azure

In this task, you will be reviewing the code in the visual studio code and publishing the application to Azure App Services through CLI.

1. In the LabVM, open **File Explorer** naviagte to the `C:\LabFiles\OpenAIWorkshop-Automation\scenarios\incubations\automating_analytics` **(1)** path, right click on **app.py (2)**, and select **Open with Code (3)**. Take a look at the code to see how it works.

   ![](images/file-select.png "Azure OpenAI")

   - The provided code is a Streamlit application that consists of two main components: a SQL Query Writing Assistant and a Data Analysis Assistant. The application allows you to interact with an SQL database and perform various tasks.

   - The code begins with importing necessary libraries and dependencies such as Streamlit, Pandas, NumPy, Plotly, and others. It also imports custom modules like AnalyzeGPT, SQL_Query, and ChatGPT_Handler.
  
1. If the pop up appears for **Do you trust the authors of the file in this folder**, click on **Yes, I trust the authors.**

   ![](images/sql10.png "Azure OpenAI")

1. In the code snippet, you can configure Azure OpenAI deployment settings and optional SQL Server settings. It provides input fields for entering deployment names, endpoints, API keys, and SQL Server details. With Streamlit, you can save settings and customize the application's functionality. Settings allow you to customize the application's behavior based on your specific needs, enhancing the overall experience.

   ![](images/code01.png "Azure OpenAI")

1. The code snippet creates a chat interface using two GPT models, "ChatGPT" and "GPT-4". There are various models to choose from, FAQs specific to each model, and a form to ask questions. Moreover, the code includes options for showing the code and prompts, allowing you to interact with the chat interface more easily.

   ![](images/code02.png "Azure OpenAI")

1. There is a "Submit" button in the code snippet that triggers a series of checks and actions. It verifies that the necessary deployment settings and SQL server settings are provided. If all requirements are met, it creates an SQL query tool and an analyzer object. To run queries and display results, it uses different methods based on the index value.

   ![](images/code03.png "Azure OpenAI")   
      
1. In the LabVM, navigate to Desktop and search for `cmd` in the search box then click on **Command Prompt**.

   ![](images/sql11.png "Azure OpenAI")

1. Run the below command to change the directory.

   ```bash
   cd C:\LabFiles\OpenAIWorkshop-Automation
   ```

1. Run the below command to **Authenticate with Azure**. It will redirect to Azure authorize website, select your account.

   ```bash
   azd auth login
   ```

    >**Note:** The warnings can be ignored.

   ![](images/sql12.png "Azure OpenAI")

1. Run the below command to setup the resource group deployment and **Create a new environment**. Make sure to replace `{DeploymentId}` with **<inject key="Deployment ID" enableCopy="true"/>** in the below command.

   ```bash
   azd config set alpha.resourceGroupDeployments on
   ```
   
   ```bash
   azd env new sql-chat-gpt-{DeploymentId}
   ```

1. Run the below command to Provision Azure resources, and deploy your project with a single command.

   ```bash
   azd up
   ```

1. Please select your Azure Subscription to use, enter `1` and click on the **Enter** button.

      ![](images/app-sub.png "Azure OpenAI")

1. Please select an Azure location to use, select the location as **<inject key="Region" enableCopy="false"/>** location, and click on the **Enter** button. You can change the location using the up and down arrow.

   ![](images/sql13.png "Azure OpenAI")

1. Once the deployment succeeded, you will see the following message **SUCCESS:  Your up workflow to provision and deploy to Azure completed**. The deployment might take 5 - 10 minutes. It is producing a web package file, then creating the resource and publishing the package to the app service.

      ![](images/im4.png "Azure OpenAI")

1. Navigate back to the Azure portal, search and select **App services**. 

      ![](images/sql14.png "Azure OpenAI")

1. Select the available web app that you have deployed in the previous step.

      ![](images/app-service-select.png "Azure OpenAI")

1. Next, click on **Browse** to open your Web application.

      ![](images/webapp.png "Azure OpenAI")
      
      ![](images/webapp2.png "Azure OpenAI")

    > **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
   - If you receive a success message, you can proceed to the next task.
   - If not, carefully read the error message and retry the step, following the instructions in the lab guide.
   - If you need any assistance, please contact us at cloudlabs-support@spektrasystems.com. We are available 24/7 to help you out.
 
   <validation step="d47c14c0-5c3c-489c-9872-959b900195b5" />
   
## Summary

In this exercise, you have covered the following:
-  OpenAI Setup and hosted a demo application to Azure. 
   
### You have successfully completed the exercise
