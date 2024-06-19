---
title: Register Human Adult Data with the Human Atlas Reference
permalink: /docs/register-human-atlas-reference/
---

This page includes directions to register human data with HuBMAP's RUI tool integrated into ATLAS-D2K. The Registration User Interface (RUI) supports spatially registering human tissue blocks to a 3D reference organ in the HRA using the Common Coordinate Framework (CCF) Registration User Interface (RUI) from HuBMAP.

You can find the [**video tutorial** for using this tool here](https://www.youtube.com/watch?v=gY3_-LIoKaU).

![Linking accounts page]({{ "/assets/img/rui-start-registration.jpg" | relative_url }})
_The "Start registration" page_

![Linking accounts page]({{ "/assets/img/rui-registration-interface.jpg" | relative_url }})
_The main RUI registration interface_

1. With your Specimen record in edit mode, scroll down to find the _HRA 3D Coordinate_ field and click "Select a value" to choose an “HRA 3D Coordinate”.
2. Click the _Create new_ button on the top right of the table.
3. In the "Name" field, add a logical name for the coordinate.
4. Click "Select a value" in the Registration UI field to open the **CCF-RUI** tool.
5. Fill in the fields and click "Start Registration".
6. Enter the values in the RUI tool: set the Anatomical Structure, and indicate the location of the sample by dragging the square into the correct location of the organ. The RUI interface offers two ways of navigation: 2D (**Register**) and 3D (**3D Preview**):
    1. Under the 2D option, which is the default option named **Register**, you can switch between four different views of the organ (Left, Right, Anterior, Posterior) and use your mouse to drag and drop the virtual square to the correct location.
    2. Under the **3D Preview** option, you can use your mouse to rotate the organ in three dimensions and use keyboard shortcuts to move the block ("W" and "S" for up-down, "D" and "A" for right-left, and "Q" and "E" for anterior-posterior).<br/>Once you are finished, click "Review and Register" and then "Register". This will close the popup and display the ID of your registry.
7. After choosing the appropriate values for other fields, click the _Save_ button. If there weren’t any errors, you will be redirected to the record page of the HRA 3D Coordinate you created.
8. Find the Specimen form tab that you were working on. Upon focusing on the page, the displayed option on the popup should update so you can see the newly created record.
9. Click the "Select" button (the blue button with the checkmark icon) on the row corresponding to the newly created HRA 3D Coordinate. The popup should close, and you should see the name of your registry on the HRA 3D Coordinate field.

You can now click on the Save button to save your changes. If there weren’t any errors, you will be redirected to the record page of the Specimen.

### 6.1 Editing an existing HRA 3D coordinate

1. Go to the Specimen page and make sure you are logged in.
2. From the "Refine search" sidebar, find the "HRA 3D Coordinate" filter and open it (it’s the second to last option).
3. Choose the "All records with value" option. The results table will now only display Specimen records that include HRA 3D Coordinate data.
4. You can choose a specific coordinate you want to edit instead of "All records with value".
5. Open any Specimen records by clicking on the “View” icon (document with magnifying glass icon).
6. In the opened Specimen record page, you should see the "HRA 3D Coordinate" field. Click on the field value, which is a link to the HRA 3D Coordinate record.
7. In the opened HRA 3D Coordinate record page, use the Edit button to navigate to the edit mode.
