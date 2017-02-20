---
title: Lab 0 - Setup IBM API Connect
toc: true
sidebar: labs_sidebar
permalink: /lab0.html
summary: In this lab, you’ll setup a Bluemix account and enable API Connect service on your account.
---

## Objective
In the following lab, you will learn:

+ SignUp a Bluemix account
+ How to enable API Connect on your Bluemix account

## Step by Step Lab Instructions

### 0.1 - Create your Bluemix account

If you already has a Bluemix account, jump to section 0.3 - Enable the API Connect Service on your Bluemix Account

1.  Open a browser and visit:

    [http://www.bluemix.net](http://www.bluemix.net)

1.  Press the SIGN UP button

    ![](https://github.com/ibm-apiconnect/pot/raw/gh-pages/images/lab1/mac-bluemix-setup.png)

1.  Complete the form and press the CREATE ACCOUNT button

    ![](https://github.com/ibm-apiconnect/pot/raw/gh-pages/images/lab1/mac-bluemix-setup-account-details.png)

1.  Check your email for your next steps.

    ![](https://github.com/ibm-apiconnect/pot/raw/gh-pages/images/lab1/mac-bluemix-setup-confirmation-email.png)

1.  Open the email and click the Confirm your account link.

    ![](https://github.com/ibm-apiconnect/pot/raw/gh-pages/images/lab1/mac-bluemix-setup-confirmation-email-detail.png)

1.  Once confirmed, you will be taken to a page that says Success! To login, click the Log In link

1.  Enter your email address and press the CONTINUE button

1.  Then enter your password on the next page and press the LOG IN button

1.  Once you are logged in, you can start your 30 day trial by clicking on the launch button.

	![](https://github.com/ibm-apiconnect/pot/raw/gh-pages/images/lab1/mac-bluemix-launch-trial.png)

2. You will be prompted to create an organization. Enter an organization name (notice that there are suggestions for you). Also select an appropriate region. Then press the CREATE button.

    ![](https://github.com/ibm-apiconnect/pot/raw/gh-pages/images/lab1/mac-bluemix-setup-create-org.png)

1.  Next you will be prompted to create a space such as dev, test, prod, etc. You can name it whatever you would like (again notice the recommendations). Then press the CREATE button.

    ![](https://github.com/ibm-apiconnect/pot/raw/gh-pages/images/lab1/mac-bluemix-setup-create-space.png)

1.  Next you will see the Summary page where you can review your entries. Press the I'm Ready button

    ![](https://github.com/ibm-apiconnect/pot/raw/gh-pages/images/lab1/mac-bluemix-setup-summary.png)

1.  You will see a screen then that  Click the `Catalog` button to go to your catalog and create your API Connect instance in section 0.3 below.

    ![](https://github.com/ibm-apiconnect/pot/raw/gh-pages/images/lab1/mac-bluemix-setup-complete.png)

### 0.3 - Enable the API Connect Service on your Bluemix Account

1.  Once in the catalog, you can search for the API Connect service by entering in `API Connect` in the search box next to the magnifying glass icon.  Click on the `API Connect` Icon to install a new instance of API Connect into your Bluemix space.

    ![](http://github.com/ibm-apiconnect/pot/raw/gh-pages/images/lab1/28.png)

1.  You can read through some of the details about the service.  You can fill in the information based on your needs.
	- SPACE – The name of your Bluemix Space to deploy the API Connect Service
	- APP – Keep the default “Leave unbound”
	- Service Name – The name you want to give to your API Connect implementation if required
	- Selected Plan – Keep the default  Once you are ready to continue, Click the `Create` button.

    ![](http://github.com/ibm-apiconnect/pot/raw/gh-pages/images/lab1/29.png)

1.  The API Connect service is now deployed.  Return to your Dashboard and you will see that your API Connect service is there.  Click on it open.

    ![](http://github.com/ibm-apiconnect/pot/raw/gh-pages/images/lab1/33.png)

1.  It will log into your instance for you automatically.  Once finished, it should drop you in your Drafts window.  

    ![](http://github.com/ibm-apiconnect/pot/raw/gh-pages/images/lab1/34.png)

1.  Click on the Navigate button in the upper left corner and select `Dashboard`.  If you see your `Sandbox` catalog there, then the process to create your instance is complete.

	![](http://github.com/ibm-apiconnect/pot/raw/gh-pages/images/lab1/34a.png)


## Conclusion

In this lab you learned:

+ Set up your Bluemix Account.
+ Enable API Connect in Bluemix.
