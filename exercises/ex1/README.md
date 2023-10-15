# Exercise 1 - Creating Business Users in SAP S/4HANA Cloud

In this exercise, we will create our first business users in SAP S/4HANA Cloud. Therefore, we will explore two different identity management scenarios for creating business users. 

Depending on the setup of your IT landscape, choose between different identity management scenarios for your SAP S/4HANA Cloud system. The identity management scenarios differ with regard to the leading system to which workers and their work agreements are onboarded as well as where the corresponding users are initially created. For more details you can check out the SAP Help documentation [Identity Management for SAP S/4HANA Cloud and Integrated Products](https://help.sap.com/docs/SAP_S4HANA_CLOUD/b249d650b15e4b3d9fc2077ee921abd0/b3a622c123b3413285eae13176d870c6.html?locale=en-US)

## Exercise 1.1 SAP S/4HANA Cloud as the Leading System for Users

In this identity management scenario, workers and work agreements are onboarded to SAP S/4HANA Cloud. The corresponding business users are initially created in SAP S/4HANA Cloud too.

1. Open the __Manage Workforce__ app.
2. Choose __Create__ and fill in at least all mandatory fields (__Last Name, Worker ID, Email__).
3. Choose __Create__.
4. After creating the basic worker, choose __Edit__.
5. Go to the __Work Agreements__ tab and choose __Create__.
6. Enter a __Start Date__ and choose __Create__.
7. Choose a __Company Code__ from the value help.
8. Fill in fields such as __Cost Center, Weekly Working Days, Weekly Working Hours,__ and so on as required. The Work Agreement ID is automatically generated.
9. Choose __Apply__ and __Save__.

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

