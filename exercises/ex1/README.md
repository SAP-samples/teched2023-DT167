# Exercise 1 - Creating Business Users in SAP S/4HANA Cloud

In this exercise, we will create our first business users in SAP S/4HANA Cloud. Therefore, we will explore two different identity management scenarios for creating business users. 

Depending on the setup of your IT landscape, choose between different identity management scenarios for your SAP S/4HANA Cloud system. The identity management scenarios differ with regard to the leading system to which workers and their work agreements are onboarded as well as where the corresponding users are initially created. For more details you can check out the SAP Help documentation [Identity Management for SAP S/4HANA Cloud and Integrated Products](https://help.sap.com/docs/SAP_S4HANA_CLOUD/b249d650b15e4b3d9fc2077ee921abd0/b3a622c123b3413285eae13176d870c6.html?locale=en-US)

## Exercise 1.1 SAP S/4HANA Cloud as the Leading System for Users

In this identity management scenario, workers and work agreements are onboarded to SAP S/4HANA Cloud. The corresponding business users are initially created in SAP S/4HANA Cloud too.

### Exercise 1.1.1 Creating Worker and associated Business Users

1. Open the __Manage Workforce__ app.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/9c270fb2d9edafbb368ec6f4165a8b6c5001b976/exercises/ex1/images/Manage_Workforce.png)

2. Choose __Create__ and fill in at least all mandatory fields (__Last Name, Worker ID, Email__). Replace XX with your participant number.

Field | Value
------------- | -------------
First Name  | John
Last Name  | S4 XX
Email  | john.s4_xx@example.com
Worker ID  | S4_JOHN_XX

3. Choose __Create__.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/56ec0b92da7cd26b32acc39a0d0f95956555d944/exercises/ex1/images/John_S4_00.png)

4. After creating the basic worker, choose __Edit__.
5. Go to the __Work Agreements__ tab and choose __Create__.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/c68d23ea002fe9be4df506acf204938a3d7a104a/exercises/ex1/images/Create_WA.png)

6. Enter a __Start Date__ and choose __Create__.

Field | Value
------------- | -------------
Start Date | 01/01/2023

7. Choose a __Company Code__ from the value help.

Field | Value
------------- | -------------
Company Code  | 1010
 
8. Fill in fields such as __Cost Center, Weekly Working Days, Weekly Working Hours,__ and so on as required. The Work Agreement ID is automatically generated.

Field | Value
------------- | -------------
Cost Center  | Financials (DE) (10101101)
Weekly Working Days  | 5
Weekly Working Hours  | 40

9. Choose __Apply__ and __Save__.
10. Choose __Maintain Business User__ button. The Maintain Business Users app is opened. A business user is automatically created with the employee data that you've just entered.
11. In the __User Data__ section, enter a __User Name__.
12. Choose __Save__.

### Exercise 1.1.2 Exporting Business User from SAP S/4HANA Cloud

1. Open the __Maintain Business Users__ app.
2. Choose __Download --> Download for IDP__. The data.csv file is available for download.

### Exercise 1.1.3 Importing User to the Identity Authentication Service

1. Open the __Identity Provider__ app. The admin console of your Identity Authentication service is displayed.
2. Open the __Import Users__ app.
  * In the __Applications__ pane, select your SAP S/4HANA Cloud system.
  * Choose __Browse__ and select the data.csv file that includes your business users.
  * To import new users to the Identity Authentication service or to update exisiting users, choose Import.
  * A confirmation dialog box is displayed notifying you about newly imported or updated users in the Identity Authentication service.
  * In the confirmation dialog box, choose __OK__.
  * To send activation e-mails to all users that are not yet active for the selected application, choose __Send__.

## Exercise 1.2 SAP Cloud Identity Services as the Leading System for Users

In this identity management scenario, workers and work agreements are onboarded to SAP S/4HANA Cloud. The corresponding users are initially created in the Identity Directory.

1.	Enter this code.
```abap
DATA(lt_params) = request->get_form_fields(  ).
READ TABLE lt_params REFERENCE INTO DATA(lr_params) WITH KEY name = 'cmd'.
  IF sy-subrc <> 0.
    response->set_status( i_code = 400
                     i_reason = 'Bad request').
    RETURN.
  ENDIF.

```

2.	Click here.
<br>![](/exercises/ex1/images/01_02_0010.png)


## Summary

You've now ...

Continue to - [Exercise 2 - Exercise 2 Description](../ex2/README.md)

