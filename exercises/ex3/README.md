# Exercise 3 - Quiz

In this exercise, we will test your knowledge by going through some example use cases. 

## Exercise 3.1 Business Users

<details>
  <summary>Is there any best practice with regards to Identity Management in SAP S/4HANA Cloud and integrated products?</summary>
  <p>Yes, check the guide in the <a href="https://help.sap.com/docs/SAP_S4HANA_CLOUD/b249d650b15e4b3d9fc2077ee921abd0/b3a622c123b3413285eae13176d870c6.html?locale=en-US">documentation.</p>
</details>

<details>
  <summary>Can we configure periodic jobs to lock inactive business users?</summary>
  <p>Yes, please check <a href="https://help.sap.com/docs/SAP_S4HANA_CLOUD/55a7cb346519450cb9e6d21c1ecd6ec1/a817aef3b51d4b0fbc4907e7adcfacd7.html?locale=en-US">How to Lock Unused Business Users
</a></p>
</details>

## Exercise 3.2 Business Roles

<details>
  <summary>We need to make sure that key users can assign specific business roles to specific users. Can this scenario be implemented?</summary>
  <p>Yes, please check <a href="https://help.sap.com/docs/SAP_S4HANA_CLOUD/55a7cb346519450cb9e6d21c1ecd6ec1/24f5b79256f64990af35b22ea87ea020.html?locale=en-US">Maintain Business User Groups</a> and <a href="https://help.sap.com/docs/SAP_S4HANA_CLOUD/55a7cb346519450cb9e6d21c1ecd6ec1/72b48dea7743487c952fa13fbdb6d23c.html?locale=en-US">Maintain Business Role Groups</a></p>
</details>

<details>
  <summary>Are there any best practices with regards to business role design in SAP S/4HANA Cloud?</summary>
  <p>Yes, check the <a href="https://go.support.sap.com/roadmapviewer/#/group//roadmapContentPage/82b2db84548d41209cda972f0fac428b:t4">SAP Activate Roadmap</a> in particular the task <a href="https://go.support.sap.com/roadmapviewer/#/group//roadmap/82b2db84548d41209cda972f0fac428b:t4/node/FA163ED752201EDABFE83D4F5A9A3D51:t4/FA163ED752201EDABFE83D2925E11D51:t4"> Plan and Design Identity and Access Management.</p>
</details>

<details>
  <summary>Are there any best practices with regards to management of business roles during and after release upgrades of SAP S/4HANA Cloud?</summary>
  <p>Yes, SAP provides guidance with the SAP S/4HANA Cloud Identity and Access Management Release Activities guide in the <a href="https://support.sap.com/content/dam/SAAP/SAP_Activate/S4H_1072%20SAP%20S4HC%20IAM%20Release%20Activities%20_%203SL.pdf"> SAP Activate Roadmap.</p>
</details>

## Exercise 3.3 Business Catalogs

<details>
  <summary>Is it possible to see which scope item my business catalogs depend on?</summary>
  <p>Yes, check the Business Catalogs app on tab Scope Items. Alternatively, use the IAM Information System app (Main Entity: Business Catalog, tab: Business Catalog - Scope Item).</p>
</details>

<details>
  <summary>The business catalog is marked as not scope-dependent. What does this mean?</summary>
  <p>Business catalogs that do not depend on any scope items are always visible in the system. For these business catalogs, the following message appears in the table: The business catalog is not scope-dependent.</p>
</details>

<details>
  <summary>How shall I handle deprecated business catalogs?</summary>
  <p>Due to ongoing development in SAP S/4HANA Cloud, including the development of new features and new apps, we need to revise existing business catalogs periodically. This means that some business catalogs will be deprecated and replaced by new ones. You will need to assign roles and users to these new catalogs. Rather than disappearing, such business catalogs are marked as deprecated, which allows you to identify them at a glance. You can also check how many deprecated business catalogs you still have in use with the Business Catalogs app. This app lets you change assignments from the old, deprecated business catalogs to the new, active catalogs quickly and easily. Once the deprecation of a business catalog is announced with the Business Catalogs app, the catalog stays in the system for at least 6 months before being deleted. During these at least 6 months, you can use the old or the new business catalogs. Within this timeframe, you can replace them when it suits you best. In the Business Catalogs app, you can see the release in which the deprecation of a business catalog was announced. In SAP S/4HANA Cloud, some business catalogs are redesigned in each release. Please check the assignments for your roles and users in the Business Catalogs app and make the necessary changes to the assignments as soon as possible..</p>
</details>

## Exercise 3.4 Restriction Types

<details>
  <summary>Are there any ways to see which restriction type is contained in which business catalogs?</summary>
  <p>Yes, use the <a href="https://help.sap.com/docs/SAP_S4HANA_CLOUD/55a7cb346519450cb9e6d21c1ecd6ec1/9203905781b441ed9359cb29803f000a.html?locale=en-US"> Display Restrction Type</a> app</p>
</details>

<details>
  <summary>I need to mass change business roles, e.g. maintain a new restriction. What is the best way to solve this issue?</summary>
  <p>Mass maintenance of business roles is possible with the mass change wizard. For more details check <a href="https://help.sap.com/docs/SAP_S4HANA_CLOUD/55a7cb346519450cb9e6d21c1ecd6ec1/07a3a58ecdbb481cab76fc4e867811cb.html?locale=en-US">How to Make Mass Changes to Business Roles</p>
</details>

<details>
  <summary>My end users are complaining that they are getting authorization failed issues. Is there a tool to trace authorizations?</summary>
  <p>Yes, please check the Display Authorization Trace app. For more details check the <a href="https://help.sap.com/docs/SAP_S4HANA_CLOUD/55a7cb346519450cb9e6d21c1ecd6ec1/79b3c9b7701248fe83b81d4b15134e8d.html?locale=en-US">documentation</p>
</details>

## Exercise 3.4 Reporting

<details>
  <summary>Where can I find the list of users which have not been active in the last 3 months?</summary>
  <p>Please check the <a href="https://help.sap.com/docs/SAP_S4HANA_CLOUD/55a7cb346519450cb9e6d21c1ecd6ec1/f249696fdfb8401eb18cf3ade365b8c1.html?locale=en-US"> IAM Key Figures</a> app</p>
</details>

<details>
  <summary>Is there a way to find out which users have access to a specific app?</summary>
  <p>Please check the <a href="https://help.sap.com/docs/SAP_S4HANA_CLOUD/55a7cb346519450cb9e6d21c1ecd6ec1/82d17cfdb0f3464b9735e4ded705f71f.html?locale=en-US"> IAM Information System</a> app. Change the Main Entity to Application.</p>
</details>

## Summary

__Congratulations__! You've completed all exercises.
