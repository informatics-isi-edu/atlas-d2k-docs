---
title: Using the Annotation Tool
permalink: /docs/annotating-images/
---

This capability allows ATLAS-D2K members to annotate imaging data to visually indicate specific anatomical regions relating to ontological terms. These annotations then link out to the corresponding anatomy page for that region which displays more information on the region and lists any related data in the ATLAS-D2K repository.

We offer two paths for annotation: online from your web browser or offline via a third-party tool called [QuPath](https://qupath.github.io/).

## Online annotation in the Data Browser

Scroll down for more specific directions with screenshots. In general, members with editing rights can log in, then:
* Navigate to the image of choice (click the "View Details" icon)
* Scroll down to the large image viewer.
* Click the “Show Annotation” button to open the Annotations interface. 
* Click the "New" button to start a new annotation. 
* Choose the anatomical region from the “Anatomy” field, then use the drawing tools in the blue bar to the left of the image and outline the region(s) of interest. 

NOTE: If the anatomical region you want to annotate already exists, but there are additional annotations you want to make, make sure to edit the existing annotation (click the pencil/Edit icon) instead of starting a new one. This ensures they all use the same color (for identification purposes). 

A "Comments" field allows you to enter more information about your annotation, which you can format for readability.

Then set the required fields: *Curation Status, Principal Investigator and Consortium*.

Note about "Curation Status": The default "In Preparation" will keep it hidden in Draft mode while you complete your work. When you’re ready, choose "Submitted" for a brief review via the Hub. You also have the option to go ahead and choose “Released” for public access.

## Offline annotation with QuPath

 [QuPath](https://qupath.github.io/) is a useful tool to use for more complex annotations or if you just prefer to work offline. Now you can take your image (or download one from the ATLAS-D2K repository), annotate it in QuPath (with x, y, z caveats) and then upload it back to the website where it will be available for viewing by the public along with the original file.

## How to Annotate an Image

- [Online annotation in the Data Browser](#online-annotation-in-the-data-browser)
- [Offline annotation with QuPath](#offline-annotation-with-qupath)
- [How to Annotate an Image](#how-to-annotate-an-image)
  - [Add a new Annotation](#add-a-new-annotation)
  - [Edit/Delete an existing Annotation](#editdelete-an-existing-annotation)
  - [Draw a Shape](#draw-a-shape)

### Add a new Annotation

1. Make sure that you are logged in.

2. On the left hand side, beside the image you will see a `New` button. Click on it to open the `Create annotation` panel.

	![]({{ "/assets/wiki_images/annotation_tools/NewButton.png" | relative_url }})

	![]({{ "/assets/wiki_images/annotation_tools/CreateAnnotationPanel.png" | relative_url }})

3. Fill in the following fields:

	- Select the related anatomical term in the `Anatomy` field. (Required)

	- Enter any useful description of your annotation in the `Comments` field. You may format your text using the formatting icons above the field. (Optional)

	- The `Curation Status` field is `In Preparation` by default, which means it is not viewable to the public. You may change this field to `PI Review` if your lab uses that status for internal review or to `Submitted` to send it to the Hub for biocuration and subsequent release to the public.

	- Select the relevant `Principal Investigator`. (Required)

	- Select the relevant `Consortium`. (Required)

5. Select the desired annotation shape from the `Annotation Toolbar`. You may choose from pencil icon (freehand drawing), rectangle or circle.

	![]({{ "/assets/wiki_images/annotation_tools/AnnotationToolbar.png" | relative_url }})

6. Draw the shape in the desired location on the image. (You may use multiple and different shapes within the annotation). See [Draw a shape](#draw-a-shape) for more details about the different drawing options.

7. You may de-select the current shape by click on the same shape from the `Annotation Toolbar`.

8. To save your annotation, click on the `Save` button in the `Create annotation` panel.

	![]({{ "/assets/wiki_images/annotation_tools/SaveButton.png" | relative_url }})

### Edit/Delete an existing Annotation

1. Make sure that you are logged in.

2. Click on the `Edit Annotation` icon of the annotation that you want to edit.

SCREENSHOT

3. To change the color of the annotation, pick a different color from the color picker (red square). This will change the color of all the shapes of the annotation that share the original color.

![]({{ "/assets/wiki_images/annotation_tools/ColorPicker.png" | relative_url }})

4. To delete a shape from this annotation, select the `Erase` tool from the annotation toolbar and click on the shape that you want to delete.

5. To add a new shape, select the shape that you want from the annotation toolbar and start drawing it on the image.

6. After you are done making your changes, click on the `Save` button in the `Edit annotation` panel.

7. To delete the entire annotation, click on the `Delete` button in the `Edit annotation` panel.

	![]({{ "/assets/wiki_images/annotation_tools/DeleteButton.png" | relative_url }})

### Draw a Shape

1. Select the tool from the annotations toolbar. You choices include: path (pencil icon, where you can use your mouse to draw the shape), rectangle, circle or polygon.

	![]({{ "/assets/wiki_images/annotation_tools/Path.png" | relative_url }})

2. For most tools, you’ll press and hold the left mouse button where you want to start drawing the shape on the image. Then drag the mouse to draw the shape to your desired dimensions and let go of the button to stop drawing the shape. With the path (pencil) tool, you’ll press and hold the left mouse button at the starting point and keep dragging the mouse in the desired path until you come back to the original point and then let go of the button.

3. To add subsequent paths, repeat steps 2 & 3.

4. When you are finished with adding paths, click Save.

