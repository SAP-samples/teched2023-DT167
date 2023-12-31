# Prerequisites

In this exercise, you will check if you can generally access the SAP systems for completing the subsequent exercises.

## Access SAP S/4HANA Cloud System

First, we will log in the SAP S/4HANA Cloud system.

1. Open the SAP S/4HANA Cloud [system](https://my301361.s4hana.ondemand.com/ui#Shell-home)
2. Enter your credentials to access the SAP S/4HANA Cloud system
3. Open the __Maintain Business User__ app.
<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/0758ae69f7d54ebf181bcdeaf6c8a6c7ee731e67/exercises/ex0/images/Maintain_Business_User_app.png)
4. Select your business user.
5. Verify that the business role __Administrator__ (_SAP_BR_ADMINISTRATOR_) is assigned to your business user. The business roles assigned to your business user are displayed in the __Assigned Business Roles__ section.

__Note:__ The SAP business role template _SAP_BR_ADMINISTRATOR_ is the only business role which is delivered in the SAP namespace and is not designed to be used productively in productive scenarios. We are using it for this exercise only!

6. Open the business role and navigate to the __Assigned Business Catalogs__ tab. Verify that the following business catalogs are assigned to the business role:
  * __Master Data - Manage Workforce__ (_SAP_BUM_BC_MNG_WORKFORCE_PC_)
  * __Security - Identity Provider__ (_SAP_CORE_BC_SEC_IDP_PC_)
  * __Identity and Access Management - Role Management__ (_SAP_CORE_BC_IAM_RM_)
  * __Identity and Access Management - Role Assignment__ (_SAP_CORE_BC_IAM_RA_)
  * __Identity and Access Management - User Management__ (_SAP_CORE_BC_IAM_UM_)
  * __User Interface - Configuration__ (_SAP_CORE_BC_UI_)
  * __User Interface - Fiori Launchpad Design__ (_SAP_CORE_BC_UI_FLD_)  
<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/28f4880eec6416ca420457c4936a7071a38cb57d/exercises/ex0/images/BC_IDP.png)

7. Open the __Manage Launchpad Settings__ app. Verify that the toggle for the Spaces is turned __ON__.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/e5ae6697c85756eba45c244dc25132156d0db46e/exercises/ex0/images/Spaces_on.png)

8. Open the __Settings__. You need to click on the user icon (top right) and select Settings. Verify that the __Use Spaces__ is enabled.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/86e7eb36b04da709a47f98585978d533438127c8/exercises/ex0/images/use_spaces.png)

## Access SAP Cloud Identity Services - Identity Authentication

Second, we will navigate to the Identity Authentication service via the SAP S/4HANA Cloud system.

1. Open the __Identity Provider - Admin Console__ app. The admin console of the Identity Authentication service opens up in a separate browser tab.
2. Open the __Administrators__ app.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/6e5509fe1f84a670cc2eedf9204b32252403a510/exercises/ex0/images/Verify_IAS_admin.png)

3. In the list of administrators, search for your user (e.g. TECHED_XX). Verify that the authorization __Manage Identity Provisioning__ is assigned to __On__.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/8cd448bdded891bbd4337b6ee00dd751d1e07fbc/exercises/ex0/images/Verify_IPS_auth.png)

## Access SAP Cloud Identity Services - Identity Provisioning

Finally, we will navigate to the Identity Provisioning service. We will verify that necessary source and target systems are set up for user provisioning.

1. Open the __Source Systems__. You will find it in the __Identity Provisioning__ section.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/2ed507b05be0ec535ecf4dd7fc0bb2f17f9a5552/exercises/ex0/images/IPS_source_system.png)

2. The list of pre-configured source systems is displayed. Verify you can see the following source systems
   * IAS formy301361 - source
   * S4-my301361-source

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/0a1fa1e8da9754b569415702949a19a82df0af65/exercises/ex0/images/Verify_ips_source_systems.png)

3. Open the __Target Systems__. You will find it in the __Identity Provisioning__ section.

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/6930836a81ac06e4d1c3bf5d9edf405e4002b910/exercises/ex0/images/IPS_target_system.png)

4. The list of pre-configured target systems is displayed. Verify you can see the following target systems
   * S4HANAmy301361 - target
   * SAC-my301361-target

<br>![](https://github.com/SAP-samples/teched2023-DT167/blob/23da9f3ac061441a11fc60078e6ec0800b020737/exercises/ex0/images/Verify_ips_target_systems.png)

## Summary

Now that you have verified your access to the SAP systems, we can continue with [Exercise 1 - Creating Business Users in SAP S/4HANA Cloud](../ex1/README.md)
