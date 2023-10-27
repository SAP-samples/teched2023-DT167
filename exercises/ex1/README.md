# Exercise 1 - Creating Business Users in SAP S/4HANA Cloud

In this exercise, we will create our first business users in SAP S/4HANA Cloud. Therefore, we will explore two different identity management scenarios for creating business users. 

Depending on the setup of your IT landscape, choose between different identity management scenarios for your SAP S/4HANA Cloud system. The identity management scenarios differ with regard to the leading system to which workers and their work agreements are onboarded as well as where the corresponding users are initially created. For more details you can check out the SAP Help documentation [Identity Management for SAP S/4HANA Cloud and Integrated Products](https://help.sap.com/docs/SAP_S4HANA_CLOUD/b249d650b15e4b3d9fc2077ee921abd0/b3a622c123b3413285eae13176d870c6.html?locale=en-US)

## Exercise 1.1 First Business User Creation in SAP S/4HANA Cloud

In this identity management scenario, workers and work agreements are onboarded to SAP S/4HANA Cloud. The corresponding business users are initially created in SAP S/4HANA Cloud too.

__Note:__ For development, test, and production systems, we recommend that you do not download the CSV file, to authenticate your users. Instead of downloading the CSV file and uploading it to the Identity Authentication service, you can set up the Identity Authentication service so that it acts as a proxy to delegate the authentication to your corporate identity provider.

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

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/7b4c0d039c42fa26d920d64f3aa9e2e85550f0a1/exercises/ex1/images/WA_Details.png)

10. Choose __Maintain Business User__ button. The Maintain Business Users app is opened. A business user is automatically created with the employee data that you've just entered.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/0c0eec74f04761751ed356c40e98f207567219c2/exercises/ex1/images/Manage_workforce_maintain_business_user.png)

11. In the __User Data__ section, enter a __User Name__ (e.g. S4_JOHN_XX).

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/0427a4fc35a9c400abc82e970895d58cd8d642a6/exercises/ex1/images/Maintain_business_user_user_name.png)

12. Choose __Save__.

### Exercise 1.1.2 Exporting Business User from SAP S/4HANA Cloud

1. Open the __Maintain Business Users__ app.
2. Search for your newly created business user by entering the User Name __S4_JOHN_XX__ in the __User Name__ search field. Click __Enter__.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/5c10606cf36d46ddde62e5500d83e3e7e05cc37a/exercises/ex1/images/Maintain_business_user_s4_john.png)

3. Choose __Download --> Download for IDP__. The data.csv file is available for download.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/bb70ef252995d409079ebd27110f3826a773fdc0/exercises/ex1/images/Download_for_idp.png)

### Exercise 1.1.3 Importing User to the Identity Authentication Service

1. Open the __Identity Provider__ app. The admin console of your Identity Authentication service is displayed.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/5b72b1c486154c6661a04d92ee6173ee4c78827b/exercises/ex1/images/IDP_Admin_console.png)

2. Open the __Import Users__ app.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/bc3916d7c1008e861469c47beccaf75a3aebc8f2/exercises/ex1/images/Import_users.png)

  * In the __Applications__ pane, select your SAP S/4HANA Cloud system.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/ed3b13c548fde8834271b1410908d1ca06c2dc36/exercises/ex1/images/Import_users_s4_application.png)
  
  * Choose __Browse__ and select the data.csv file that includes your business users.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/d3d4866ca4b12be6b777ba03d4ec14fecd80fdd8/exercises/ex1/images/Import_users_browse.png)
  
  * To import new users to the Identity Authentication service or to update exisiting users, choose __Import__.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/778b06651747dd761344648b2c05a1c4aba71eec/exercises/ex1/images/Import_users_import.png)
  
  * A confirmation dialog box is displayed notifying you about newly imported or updated users in the Identity Authentication service.
  * In the confirmation dialog box, choose __OK__.
  * To send activation e-mails to all users that are not yet active for the selected application, choose __Send__.

## Exercise 1.2 SAP Cloud Identity Services as the Leading System for Users

### Exercise 1.1.1 Creating Worker and Work Agreement

In this identity management scenario, workers and work agreements are onboarded to SAP S/4HANA Cloud. The corresponding users are initially created in the Identity Directory.

1. Open the __Manage Workforce__ app.

2. Choose __Create__ and fill in at least all mandatory fields (__Last Name, Worker ID, Email__). Replace XX with your participant number.

Field | Value
------------- | -------------
First Name  | John
Last Name  | CIS XX
Email  | john.cis_xx@example.com
Worker ID  | CIS_JOHN_XX

3. Choose __Create__.
4. After creating the basic worker, choose __Edit__.
5. Go to the __Work Agreements__ tab and choose __Create__.
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

### Exercise 1.1.2 Creating User in Identity Authentication Service

1. Open the __Identity Provider__ app. The admin console of your Identity Authentication service is displayed.
2. Choose the __User Management__ tile.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/a48b0c07fb9c86da945abbebec6c16b3d28d9314/exercises/ex0/images/IAS_user_management.png)

3. The system displays the first 20 users in the tenant sorted by their user ID number.
4. Press __Add__.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/e1b66aa576bd081828d8c9df45ef4071e2f6841a/exercises/ex0/images/IAS_add_user.png)

5. Fill in the required fields in the dialog box.

Field | Value
------------- | -------------
First Name  | John
Last Name  | CIS XX
Email  | john.cis_xx@example.com
Login Name  | CIS_JOHN_XX
User Type  | Employee
Account Activation  | Set status active

6. Search for the newly created user and click on __Edit__.
7. Click the checkbox __Verify Email__ and enter the __Employee Number__ CIS_JOHN_XX.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/0486ee3b97cff772afc94049708c25f2c7c358cf/exercises/ex1/images/Verify_email_employee_number.png)

### Exercise 1.1.3 Running Provisioning Job in the Identity Provisioning Service

1. Open the Identity Authentication service administration console. Go to __Source Systems__.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/28b4e78528b58655ec5629eaee8088fbe8668024/exercises/ex0/images/IPS_source_system.png)

2. Select the source system __IAS formyXXXXXX - source__.
3. Go to the __Jobs__ tab.
4. For Job Type __Read Job__ select the __Run Now__ action.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/becf9e88763253dda7e6449305c04c9128883f9d/exercises/ex1/images/IPS_Read_job.png)

5. Go to __Provisioning Logs__ and verify that the IPS job was executed successfully and 1 business user was created in SAP S/4HANA Cloud

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/7916963877a1f04aa7c05f5027030b2138e7364c/exercises/ex1/images/IPS_1_user_created.png)

6. Verify in the SAP S/4HANA Cloud system that the business user is created.
   * Open the __Maintain Business User__ app. Search for the __User Name__ CIS_JOHN_XX.
   * Open the newly created business user.
   * Verify that the User Name and Global User ID are populated, with the same values from the Identity Authentication Service.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/4365eb4bfc1440e61cbca3fde74132580e5d6b4b/exercises/ex1/images/IAS_UUID_Login_Name.png)
 <br>![](https://github.com/SAP-samples/teched2023-DT167/blob/b0a69ccfcabc1cd25dc4ef7eac4cd6733b1ee813/exercises/ex1/images/Maintain_Business_User_UUID_User_Name.png)

## Summary

You've now learned two different identity management scenarios for creating business users in your SAP S/4HANA Cloud system.

Continue to - [Exercise 2 - Creating Business Roles and SAP Fiori Spaces and Pages](../ex2/README.md)

