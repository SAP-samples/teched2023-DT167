# Prerequisites

In this exercise, you will check if you can generally access the SAP systems for completing the subsequent exercises.

## Access SAP S/4HANA Cloud System

First, we will log in the SAP S/4HANA Cloud system.

1. Go to https://myXXXXXX.s4hana.cloud.sap/ui#Shell-home
2. Enter the following User Name and Password to access the SAP S/4HANA Cloud system
   * __User Name__: TECHED_XX
   * __Password__: TECHED_XX
3. 

## Access SAP Cloud Identity Services - Identity Authentication

Second, we will navigate to the Identity Authentication service via the SAP S/4HANA Cloud system.

1. a
2. Click on the __Identity Provider - Admin Console__ app. The admin console of the Identity Authentication service is displayed.

## Access SAP Cloud Identity Services - Identity Provisioning

Finally, we will navigate to the Identity Provisioning service. We will verify that necessary source and target systems are set up for user provisioning.

1. Click on the __Source Systems__ tile under the __Identity Provisioning__ section.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/2ed507b05be0ec535ecf4dd7fc0bb2f17f9a5552/exercises/ex0/images/IPS_source_system.png)

2. The list of pre-configured source systems is displayed. Verify you can see the following source systems
   * IAS formyXXXXXX - source
   * S4-myXXXXXX-source

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/0a1fa1e8da9754b569415702949a19a82df0af65/exercises/ex0/images/Verify_ips_source_systems.png)

3. Click on the __Target Systems__ tile under the __Identity Provisioning__ section.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/6930836a81ac06e4d1c3bf5d9edf405e4002b910/exercises/ex0/images/IPS_target_system.png)

4. The list of pre-configured target systems is displayed. Verify you can see the following target systems
   * S4HANAmyXXXXXX - target
   * SAC-myXXXXXX-target

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/0a1fa1e8da9754b569415702949a19a82df0af65/exercises/ex0/images/Verify_ips_target_systems.png)

## Summary

Now that you have verified your access to the SAP systems, we can continue with [Exercise 1 - Exercise 1 Description](../ex1/README.md)
