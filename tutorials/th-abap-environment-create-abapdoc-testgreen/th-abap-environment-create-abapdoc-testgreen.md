---
title: Create ABAPDoc Comments in Your Class in ABAP Environment Get an overview of the multi-source landscape that we have set up and learn how to import data Test Blue
description: Long description for Test Green and testing for Roma. Learn how to maintain ABAPDoc documentation for your class in SAP Cloud Platform, ABAP Environment so your comments appear in the Outline view. Get an overview of the multi-source landscape that we have set up and learn how to import dataGet an overview of the multi-source landscape that we have set up and learn how to import data. Learn how to maintain ABAPDoc documentation for your class in SAP Cloud Platform, ABAP Environment so your comments appear in the Outline view. Get an overview of the multi-source landscape that we have set up and learn how to import dataGet an overview of the multi-source landscape that we have set up and learn how to import data. Learn how to maintain ABAPDoc documentation for your class in SAP Cloud Platform, ABAP Environment so your comments appear in the Outline view. Get an overview of the multi-source landscape that we have set up and learn how to import dataGet an overview of the multi-source landscape that we have set up and learn how to import data
auto_validation: true
time: 10
tags: [ tutorial>beginner, tutorial>community ]
primary_tag: topic>abap-development
---

## Prerequisites   
- How to maintain ABAPDoc comments
- How to synchronize comments so they appear in the Outline View
- How to add an sorted list
- How to create a link to other development object documentation within ADT

This text block is not marked as a separate section but it should be rendered after 'Prerequisites' section.

---

[ACCORDION-BEGIN [Step 1: ](Open ABAP class)]
First, open the ABAP class **`ZCL_AMDP_DEMO_XXX`** from the tutorial [Create an AMDP and Analyze Its Performance](abap-environment-amdp-profiling)

!![Image depicting step-1-open-class](step-1-open-class.png)

[DONE]
[ACCORDION-END]


[ACCORDION-BEGIN [Step 2: ](Create ABAPDoc comment)]
1. Immediately before the class definition, add an ABAPDoc comment to the class by entering **`"!`** and choosing **Auto-complete ( `Ctrl+Space` )**.

2. From the dropdown list, choose **Paragraph**, then add the following comment:

    **`"!<p>Class tests AMDP</p>`**

    !![step2a-choose-paragraph](step2a-choose-paragraph.png)

    >You must insert the ABAPDoc comment **immediately** before the declaration; otherwise you will get a warning from ADT.

3. Add the following to the paragraph ( `<p>` ) tag: **`class="shorttext synchronized"`**, so your code looks like this:

    ```
    "!<p class="shorttext synchronized">Class tests AMDP: </p>
    ```

4. Add the following comments to the table type **`ty_result_line`** and to the method **`GET_FLIGHTS`** respectively:

    ```
    "!<p class="shorttext synchronized">Table type of Flights from HANA DB</p>
    "! <p class="shorttext synchronized"> Method reads flights from HANA DB using AMDP</p>
    ```

5. Save and activate your class.

The comments should now appear in the Outline View:

!![step2b-shorttext-synch-class](step2b-shorttext-synch-class.png)

[DONE]
[ACCORDION-END]


[ACCORDION-BEGIN [Step 3: ](Add sorted list)]
1. Choose **Enter**. The system automatically inserts the ABAPDoc comments annotation `"!"` for you.

2. Again, choose **Auto-complete ( `Ctrl+Space` )**. Then choose **Sorted list**.

    !![step3a-add-sorted-list](step3a-add-sorted-list.png)

3. Add the following two statements, so that your code looks like this:

    ```
    "! <ol>
    "!    <li>Reads flights from HANA DB</li>
    "!    <li>Converts currency to EUR</li>
    "! </ol>

    ```

[DONE]
[ACCORDION-END]

[ACCORDION-BEGIN [Step 5: ](Add link)]
1. Immediately after the sorted list, choose **Enter**.

2. Now enter the following comment:

    **`"! <p>Implements the interface { @link INTF: if_oo_adt_classrun } </p>`**

This creates a link to the Element information for that interface.

[DONE]
[ACCORDION-END]


---
