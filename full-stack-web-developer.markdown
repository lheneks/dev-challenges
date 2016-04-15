## Overview
Create a simple, small web application to manage customer information.  

Treat the challenge as if you were creating a commercial, public website.

If you are more back-end focused, we will understand if it isn't the prettiest, but do your professional best to at least have it look presentable.
If you are more front-end focused we will understand if the data storage is something simple, but at least make it store somewhere.

## Minimum Business Requirements

* Add, Edit, View Customer Detail
  * Company Name
    * Required
  * Website URL
    * Optional with validation on URL format if supplied
    * If present there should be a Visit link next to the field to launch the site in a new tab/window
  * Industry 
    * Dropdown with a few common / broad industry types, required, default "- Select an Industry -"
  * Enterprise Client designation
    * Yes/No radio button group
  * Customer Contacts
    * Representing our contacts with the customer.  Should be able to add, edit and delete.
    * Screen should be a modal dialog popup on the company edit page
    * Capture first and last name, primary email address, primary phone number, Primary Contact Checkbox
all fields required, validation on email and phone format.
    * Only allow one contact to be marked primary
* View list of all customers
  * Shows Company Name, Website URL link, and Primary Contact Full Name
  * Search / filter textbox to filter list of customers by Company Name, Industry, or Contact Name
  * Button or link to Add a new Customer
* Customer List and Add/Edit should require being logged in (any type of authentication is fine)
* Static About Us page with lorem ipsum placeholder text (does not require logging in)

## Stretch Goal Business Requirements
* Allow specifying a PDF document that represents a company's signed contract with us
* Allow uploading a PDF document that represents a company's contract AND/OR
* Use a document signature service like [DocuSign](https://www.docusign.com/) or [EchoSign](https://acrobat.adobe.com/us/en/documents/esignatures.html) 
* Allow viewing the supplied PDF document either inline in a web page (ideally) or by clicking a link to download the file

## Technical Requirements
* ASP.NET 5 or ASP.NET Core 1.x should be used
* C# for backend code
* Twitter bootstrap 3+ should be used
* Data storage type and persistence up to you
* Website should ideally be a Single Page Application (SPA) using AngularJS
  * If you are unfamiliar with AngularJS you can use other js frameworks such as Knockout, Aurelia, Ember or React
  * If you don't know one of these then standard MVC may be used
* Forms authentication for login