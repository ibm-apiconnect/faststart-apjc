---
title: Lab 1 - Create API to RESTful backend
toc: true
sidebar: labs_sidebar
permalink: /lab1.html
summary: In this lab, you will learn how to create an API that connecting to a **RESTful** backend. It covers define and use **Parameter** and **Definition**, **Inline Schema** and **Map Assembly**.

---

## Objective
In the following lab, you will learn:

+ How to define input parameter and definition for the API
+ How to use the input parameter and definition in the API Assembly
+ How to create inline schema from sample JSON
+ How to use Map to create HTTP body for the RESTful backend

![](images/apjc/00.01.png)

## Case Study used in this tutorial
In this tutorial, you will be creating new API for a banking customer to initiate a fund transfer to another account. The API will accept JSON body via HTTP POST. You will need to access the parameter in url and JSON body to prepare the input parameter for the RESTful backend.

## Before you begin
For this lab, you need to have a Bluemix account and enabling the API Connect Essentials service on your account.

## Step by Step Lab Instructions

### 1.1 - Create the Transfer API Definition

1.  Go to the Drafts screen by click on ">>" to bring up the side menu and select "Drafts"

      ![](images/apjc/01.01.png)

1.  Select "APIs" tab

1.  Click "Add" and select "New API"

      ![](images/apjc/01.02.png)

1.  In the new API pop-up dialog, fill up the details as following:

  ![](images/apjc/01.03.png)

### 1.2 - Create Definitions

1.  Next, you're going to define the JSON object for the HTTP body input. The JSON object holds the transfer details.

1.  Scroll to **Definitions** section and click "+" to create new Definition.

1. Click **Add Property** 4 times and fill out the details as following:

  ![](images/apjc/02.01.png)

### 1.3 - Define Parameters

In this section, we will define 2 parameters:
  + First is the parameter in the API URI. The parameter is the user's bank account number. In the case: https://gateway/transfers/**{accountNumber}**
  + Second is the parameter in the HTTP body. The parameter is the transfer details which you have defined in the prior steps.

1.  Scroll down to **Parameters** section

1.  Click "+" to create a new parameter **accountNumber** and fill up the details as following. Do note you need to select **Path** in the Located in drop-down field.

      ![](images/apjc/03.01.png)

1.  Create another parameter **transferDetail**,  and this time will  select **Body** in the **Located in** and **Transfer** as **Type**. Do note the screen doesn't display **Transfer** even after you have selected it.

      ![](images/apjc/03.02.png)

### 1.4 - Define API Endpoint and Input

Next, we will define the API endpoint and input parameters for API consumer

1.  Scroll to **Path** section and create a new path. Enter **/{accountNumber}** as the Path.

1.  Click **Add Parameter** and select **accountNumber** from the list.

1.  Repeat the last step to add **transferDetail** parameter. Your settings should be as following:
  ![](images/apjc/04.01.png)

1.  Delete the default "Get" operation.

1.  **Add Operation** and select **Post**.


### 1.5 - API Assembly

In this section, we will learn how to use **Parameters** in the **Map** Assembly.

1.  Click on **Assemble** tab

      ![](images/apjc/05.01.png)

1.  Drag **Map** assembly and place it before **Invoke**.

      ![](images/apjc/05.02.png)

1.  Click on "+" to maximize the **Map** configuration screen.

      ![](images/apjc/05.03.png)

1.  Click on the "pencil" icon to "Edit Input"

1.  Click **+ parameters for operation...** button and select **post/{accountNumber}** operation.

      ![](images/apjc/05.04.png)

1.  Click "Done" to close the "Edit Input" screen.

1.  Click on the "pencil" icon to "Edit Output"

1.  Click on "+ outputs for operation..."

1.  Select "Inline schema" in the **Definition** drop-down

      ![](images/apjc/05.05.png)

1.  In the "Provide a schema" pop-up dialog, select "Generate from sample JSON". Copy and paste following sample JSON.


```bash
    {
      "fromAccountNumber":"123-123-123-3",
      "toAccountNumber":"123-123-123-3",
      "amount":199.99,
      "remarks":"online purchase"
    }
```
      ![](images/apjc/05.06.png)

1.  Click "Generate" button. API Connect will generate the schema in YAML format as the following screen:

      ![](images/apjc/05.07.png)

1.  Click "Done" to close the "Provide a schema" dialog.

1.  Click "Done" to close the Output.

      ![](images/apjc/05.08.png)

1.  Click **accountNumber** from Input and link to **fromAccountNumber** Output. Do the rest as following screen:

      ![](images/apjc/05.09.png)

1.  Click the X to close the Map assembly.

1.  Click on **Invoke** assembly and enter the following URL:

  ```
  http://www.mocky.io/v2/57f281c90f0000a81ae25309
  ```

      ![](images/apjc/05.10.png)

### 1.6 - Test API

In this section, we will learn how to test the API in the Assembly.

1.  Click on the "Play" button. The test panel will expand at the left.

    ![](images/apjc/06.01.png)

1.  You need to setup the **Product** for this new API. Enter **Transfers** in the new product **Name**. Click **Create and Publish** button. Then click the next button.

    ![](images/apjc/06.02.png)

1.  Select the **post/{accountNumber}** Operation to be tested

    ![](images/apjc/06.03.png)

1.  Enter a test parameter for accountNumber **123-123-123-3**. For **transferDetails**, you can click on **Generate** to let the system generate sample data automatically.

    ![](images/apjc/06.04.png)

1.  Click **Invoke** button to invoke the API. You should receive response as following:

    ![](images/apjc/06.05.png)

1.  Click on **Debug** button to inspect the assembly details:

    ![](images/apjc/06.06.png)

## Conclusion

In this lab you learned:

+ How to define input parameter and definition for the API
+ How to use the input parameter and definition in the API Assembly
+ How to create inline schema from sample JSON
+ How to use Map to create HTTP body for the RESTful backend