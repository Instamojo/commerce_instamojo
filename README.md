Instamojo-Drupal  
====
----
This module allows us to use [Instamojo](https://www.instamojo.com) as Payment Gateway with [Drupal Commerce](https://drupalcommerce.org/).

###Installation
---
- Download the [zip file](https://github.com/ashwch/commerce_instamojo/archive/master.zip) and unpack its files into a folder named **commerce_instamojo** into the modules folder of your Drupal installation. You will have to create the folder **commerce_instamojo** if not present already. The location of modules folder is `[DRUPAL-ROOT-FOLDER]/sites/all/modules/` .
    
- Browse to Drupal permission page and allow Anonymous as well as Authenticated users to use Instamojo payment gateway.
- Now go to the configuration page of Instamojo and and enable it. 
- Now click on edit to edit the configuration of the Instamojo module, there you will find 5 fields: `API Key`, `Auth Token`, `Private Salt`, `Payment Link` and `Custom Field`. The steps to find or create the required values for these fields are specified in the next sections.

### Creating a Payment Link
----
In this section we will learn how to create a `Payment link` along with how to get the required value for `Custom Field` .

- Create a Payment Link on Instamojo under the **Services/Membership** option.
  
  Set the price to Rs. 10 and enable **"Pay what you want"**.  Under **Title** and **Description**, you may enter something that describes your business and the nature of the products being sold.
  
  Under **Advanced settings** of the same link there's a field **Custom Redirection URL**, here if your website's url is **http://www.example.com** then use **http://www.example.com/response_page** as Custom Redirection URL.

 Now click on **Get started** to save the button.  Copy the current URL to the `Payment Link` in the Instamojo module configuration page of Drupal. URLs are usually of the format: `https://www.instamojo.com/<username>/<slug>/`.

- Now on Payment links's page go to **More options** and click on **Custom Fields**.

 Now create a custom field called **Order ID** and mark it as **required**. In the custom field creation page, hover over the field you just created. You'll see a field with the format **Field_**. Note down the full name (including the **Field_** bit. Note that this is case sensitive!). Enter this name in the **Custom field** field of the Instamojo module configuration page in Drupal.

###Auth
---
In this section we will learn how to get the values of fields  `API Key`,  `Auth token` and `Private salt`.

Go the [Instamojo developers](https://www.instamojo.com/developers/) page, if your are not logged in already then login first and then you'll see the value of `API Key`,  `Auth token`,  `Private salt` there on the bottom left side of the page.

Simply copy and paste their values in the configuration form in their respective fields.

Now save these settings.
