# Exercise 2 - Creating Business Roles and SAP Fiori Spaces and Pages

In this exercise, we will create our first business roles and custom SAP Fiori Spaces and Pages. 

Access to business apps is controlled by a role-based authorization management. That means you assign business roles to business users and these business roles provide access to certain business tasks. You can assign business users to business roles in the __Maintain Business Roles__ app. The main purpose of the app though is to create and adapt business roles. You create business roles by combining pre-defined __business catalogs__ that contain the actual authorizations that allow users to access apps for a specific business area. If necessary, you can change the restrictions for the access categories __value help, read, and write__ on field level. Once you have created a business role, you can assign it to multiple business users who perform similar business tasks in the Maintain Business Users.

A SAP Fiori __Space__ is the unit that holds one or more SAP Fiori __Pages__. It is assigned to you based on your work profile (__business role__). You may see several spaces in your SAP Fiori Launchpad. The spaces are displayed in the navigation bar where you can switch between the different available spaces and pages. A page is the part of the space that contains the apps as tiles and links clustered into different sections. It is shown in the main area of the launchpad. When you log on to the launchpad, you'll see the apps and sections that have been preconfigured for you. The page is your central starting point in the launchpad and should show you the apps that are relevant for the context of your daily work. Note that the pages do not show all apps you can access based on your role and the catalogs assigned to the roles, but only a selection your administrator made available. You can access all apps you are eligible to use by searching for them in the search field, in the app finder or in the All My Apps menu.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/8157e3b9c4d6d66b66e26d91c39e95001cb8e117/exercises/ex2/images/Business_roles_Spaces_Pages.png)

## Exercise 2.1 Creating Business Roles

1. Open the __Maintain Business Roles__ app.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/1a19d0889871d23432de471be513acf1a0f7bb5a/exercises/ex2/images/Maintain_business_roles.png)

2. On the initial screen, select __New__.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/93fb7756cfedfc8c3415499059b0d7bbf5a75248/exercises/ex2/images/Maintain_business_roles_new.png)

3. Add general role details.

Field  | Value
------------- | -------------
Business Role ID | Z_ROLE_TECHED_XX
Business Role Description  | Custom business role TechEd XX

4. On the __Assigned Business Catalogs__ tab, select __Add__ to add business catalogs.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/355ffe6f4126c879d083124bd3ca6f79d1e0ba42/exercises/ex2/images/Add_business_catalogs.png)

5. Add below mentioned business catalogs.

Business Catalog  | Business Catalog ID
------------- | -------------
Master Data - Manage Workforce | SAP_BUM_BC_MNG_WORKFORCE_PC
Identity and Access Management - User Management  | SAP_CORE_BC_IAM_UM
Security - Identity Provider  | SAP_CORE_BC_SEC_IDP_PC

6. Select __Apply__.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/80a4cb0a97882d3da88c479b594d8b292d55fab4/exercises/ex2/images/Add_business_catalogs_apply.png)

7. By default, the value help and read access for each business catalog is set to unrestricted and there is no write access. We change these restrictions by selecting __Maintain Restrictions__.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/f4c37ca3316c5a579bdfc90ba0032f0b2fef694e/exercises/ex2/images/Maintain_restrictions.png)

8. Change the access catagory for __Write, Read, Value Help__ and __Read, Value Help__ to __Restricted__.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/c4ea04ddaf20b47204e4a639f32da2614d38bb84/exercises/ex2/images/Access_categories.png)

9. Maintain instance-based restrictions as follows:

* __General__

Restriction Type  | Value
------------- | -------------
Company Code | 1010
User Group  | * (Unrestricted Access)
Cost Center  | * (Unrestricted Access)
Customer Account Group  | * (Unrestricted Access)
BP Role  | BUP003, BUP010
Manage Workforce Access  | 01

* __Business Partner Processing (B_BUP_DCPD)__

Restriction Field  | Value
------------- | -------------
Data Controller | * (Unrestricted Access)
Purpose  | * (Unrestricted Access)

* __Business Role User Assignment (S_BRL_ASG)__

Restriction Field  | Value
------------- | -------------
Role Group | * (Unrestricted Access)
User Group  | * (Unrestricted Access)

9. Select __Save__ to activate the business role.

## Exercise 2.2 Creating SAP Fiori Spaces and Pages

### Exercise 2.2.1 Creating SAP Fiori Spaces and assign it to Business Role

1. Open the __Maintain Business Role__ app. Select the business role __Z_ROLE_TECHED_XX__ which you created in exercise 2.1.
2. Select the __Assigned Launchpad Spaces__ tab and click on __Edit__.
3. Select __Add__. In the Assign Space to Business Role option, select __Create New Space__.
4. Enter the following details:

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/d9a1574a1fca4aaf3bdfe3cab0fda4891d3e2bc1/exercises/ex2/images/Add_launchpad_space.png)

Field  | Value
------------- | -------------
Space ID | Z_TECHED_SPACE_XX
Space Description  | Custom Space TechEd XX
Space Title  | Space TechEd XX
Create Page from Business Catalogs and Groups  | No

5. Select __Save__.

### Exercise 2.2.2 Creating SAP Fiori Pages and assign it to Space

1. Open the __Manage Launchpad Pages__ app.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/d00c7f190df601e0244efd6e86280cd02e3cc6c0/exercises/ex2/images/Manage_launchpad_pages.png)

2. Select the __Create__ button and enter the following details:

Field  | Value
------------- | -------------
ID | Z_TECHED_PAGE_WFD
Description  | Custom Page Workforce
Title  | Workforce Master

3. Confirm your input by clicking on __Create__.
4. Repeat step 2 and 3 to create two more pages with the following details:

* User Management

Field  | Value
------------- | -------------
ID | Z_TECHED_PAGE_UM
Description  | Custom Page User Management
Title  | User Management

* Security

Field  | Value
------------- | -------------
ID | Z_TECHED_PAGE_SEC
Description  | Custom Page Security
Title  | Security

5. Open the __Manage Launchpad Spaces__ app.
6. Select the space __Z_TECHED_SPACE_XX__ which you created in step 4. Select __Edit__ to assign the pages (step 7-9) to your custom space.

### Exercise 2.2.3 Designing the SAP Fiori Page Layout

1. Open the __Manage Launchpad Pages__ app.
2. Select the page __Z_TECHED_PAGE_WFD__ and click on the __Edit__ icon. You are redirected to the Page composer.
3. Enter __Workforce Master Data Management__ in the section title.
4. Add the __Manage Workforce__ app to the section by clicking on __Add__.
5. Click __Save__ to save the page layout.
6. Repeat steps 1-5 for the layout of the other pages.

## Summary

You've now ...

Continue to - [Exercise 3 - Excercise 3 ](../ex3/README.md)
