# Exercise 1 - Creating Business Users in SAP S/4HANA Cloud

In this exercise, we will create our first business users in SAP S/4HANA Cloud. Therefore, we will explore two different identity management scenarios for creating business users. Please note both identity management scenarios are valid and dependent . For more details you can check out the SAP Help documentation [Identity Management for SAP S/4HANA Cloud and Integrated Products](https://help.sap.com/docs/SAP_S4HANA_CLOUD/b249d650b15e4b3d9fc2077ee921abd0/b3a622c123b3413285eae13176d870c6.html?locale=en-US)

## Exercise 1.1 SAP S/4HANA Cloud as the Leading System for Users

After completing these steps you will have created...

1. Click here.
<br>![](/exercises/ex1/images/01_01_0010.png)

2.	Insert this line of code.
```abap
response->set_text( |Hello World! | ). 
```



## Exercise 1.2 SAP Cloud Identity Services as the Leading System for Users

After completing these steps you will have...

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

