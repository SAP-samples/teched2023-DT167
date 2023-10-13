# Prerequisites

In this exercise, you will check if you can generally access the SAP systems for completing the following exercises.

## Access SAP S/4HANA Cloud System

1. Go to https://myXXXXXX.s4hana.cloud.sap/ui#Shell-home
2. Enter the following User Name and Password to access the system

## Access SAP Cloud Identity Services - Identity Authentication



## Access SAP Cloud Identity Services - Identity Authentication

After completing these steps you will have....

1.	Click here.
<br>![](/exercises/ex0/images/00_00_0010.png)

2.	Insert this code.
``` abap
 DATA(params) = request->get_form_fields(  ).
 READ TABLE params REFERENCE INTO DATA(param) WITH KEY name = 'cmd'.
  IF sy-subrc <> 0.
    response->set_status( i_code = 400
                     i_reason = 'Bad request').
    RETURN.
  ENDIF.
```

## Summary

Now that you have ... 
Continue to - [Exercise 1 - Exercise 1 Description](../ex1/README.md)
