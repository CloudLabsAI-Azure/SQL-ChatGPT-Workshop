# Exercise 2: Quick Start With Hosted Demo Application.

### Estimated Duration : 30 minutes

In this exercise, you will be working with the application that you hosted in the previous exercise and work with the Data Analysis Assistant and SQL Query Writing Assistant in the application.

## Objectives

In this Exercise, you will complete the following task:
- Task 1: Analyzing Data Analysis Assistant and SQL Query Writing Assistant

## Task 1: Analyzing Data Analysis Assistant and SQL Query Writing Assistant

In this task, you will work with the Data Analysis Assistant and SQL Query Writing Assistant in the application.

1. When you're on the **Natural Language Query** page, click on **Settings (1)** from the left side menu. Provide the following details and then click on **Submit(6)** to save the changes.

    - ChatGPT deployment name:   **sql-chatgpt-model (2)**
    - GPT-4 deployment name:   **sql-chatgpt-model (3)**
    - Azure OpenAI Endpoint:   enter **Endpoint (4)** which you have saved in previous task.
    - Azure OpenAI Key:   enter **Key (5)** which you have saved in previous task.

       ![](images/nl-set-credential.png "Natural Language Query")

       >**Note:** You try to submit the query again in case of any errors in the output.

1. On the Natural Language Query page, select **SQL Query Writing Assistant (1)** from the left-side menu, from the **GPT model**, select **ChatGPT (2)**,  change the **FAQs** from the drop-down menu to select **Show me revenue by-product in ascending order (3)**, and and click on **Submit (4)**. According to the query, the **Output (5)** will be displayed.

    ![](images/nl-01.png "Natural Language Query")

   >**Note:** If you get an error stating that the maximum limit reached, please follow the below steps to change the model version.
     
      - Navigate to the Microsoft Edge Browser tab where Azure AI Foundry portal is opened.
     
     - From the left navigation pane click on **Deployments** (1), select the **sql-chatgpt-model** (2) and click on **Edit**(3).

         ![](images/opai-1.png)
     
     - For the Model version select **0301(Default)** option and click on **Save and close**.

         ![](images/opai-2.png)

     - Now back in the Azure portal launch the web app again from the App service resource and repeat step number 1 and 2.

1. On the **Natural Language Query** page, on the left side menu, change the **FAQs** from the drop-down menu to select **Show me top 10 most expensive products (1)**, and click on **Submit (2)**. According to the query, the **Output (3)** will be displayed.

    ![](images/nl-02.png "Natural Language Query")

1. On the **Natural Language Query** page, on the left side menu, change the **FAQs** from the drop-down menu to select **Show me net revenue by year. Revenue time is based on the shipped date. (1)**, and click on **Submit (2)**. According to the query, the **Output (3)** will be displayed.

    ![](images/nl-03.png "Natural Language Query")

1. The dropdown menu allows you to browse the rest of the **FAQs** by changing the Input value. 

7. After executing all the FAQs. Change the **Choose the app** to **Data Analysis Assistant (1)**, select the **FAQs** from the drop-down menu to select **Show me daily revenue trends in 2016 per region (2)**, and click on **Submit (3)**. According to the query, the **Output (4)** will be displayed.

    ![](images/nl-04.png "Natural Language Query")

    ![](images/z-03.png)

    ![](images/z-04.png)

1. Once you explore the output part, select the **FAQs** from the drop-down menu to select **Which products have the most seasonality in sales quantity in 2016? (1)**, and click on **Submit (2)**. According to the query, the **Output (3)** will be displayed.
 
    ![](images/nl-06.png "Natural Language Query")

    ![](images/z-05.png) 

1. Once you explore the output part, select the **FAQs** from the drop-down menu to select **Which customers are most likely to churn? (1)**, and click on **Submit (2)**. According to the query, the **Output (3)** will be displayed.

    ![](images/nl-08.png "Natural Language Query")

    ![](images/nl-09.png "Natural Language Query")
    
    ![](images/nl-10.png "Natural Language Query") 
    
    ![](images/nl-11.png "Natural Language Query")     

1. The dropdown menu allows you to browse the rest of the **FAQs** by changing the Input value.

## Summary
In this exercise, you have worked with the application that you hosted in the previous exercise and utilized the Data Analysis Assistant and SQL Query Writing Assistant in the application.

### You have successfully completed the lab     
