---
title: Requirements for Creating Schematics
permalink: /docs/requirements-for-creating-schematics/
---

The following are requirements that the graphic artists must adhere to in order to facilitate the Hub’s best use of schematics that will be used as a navigational interface into the data:

* **Scope: First phase - Organ Systems covered by GUDMAP for ****Adult**** ****Mouse:**** mus musculus, TS28**

* Organization

    * Each region should correspond to a **single term in the [GUDMAP anatomical ontology](https://www.atlas-d2k.org/chaise/recordset/#2/Vocabulary:Anatomy@sort(RID))** (for example, the anatomical region *bladder* corresponds to *EMAPA:18321*). List these in the work order spreadsheet.

    * In general, we will want overall schematics for each region made up of layers (ie path or group) that represent each of the sub-regions.

    * Each of these sub-regions must have a colored layer or group that has a name equal to the **Anatomy ID** for that anatomical region (IDs/terms will be provided in the work order spreadsheet)

# Presentation

* For each anatomical region, there should be two versions:

    *  A "grayed-out" version of the region

    * A version above it (in layer order) that is in color.

The intent is that we will programmatically show and hide the region that is in color (or "active" version) by manipulating the embedded SVG code on the web page. We will need to target the active version via the ID that will be used as the name of an enclosing layer (ie group).

* Color by tissue type: We would like standardization of the colors used for common types of structures (ie, vasculature, epithelium, etc). We don’t want to be too prescriptive yet but for an idea of the color palettes we’ve already been using historically, you can refer to [https://www.atlas-d2k.org/chaise/recordset/#2/Schematics:Schematic@sort(RID)](https://www.atlas-d2k.org/chaise/recordset/#2/Schematics:Schematic@sort(RID)) )

* Inactive color (ie the toned down version of each structure that will be visible if the active layer is turned off): For now let’s just say "gray".

* Do not add labels to the images. We will be providing them outside of the resulting SVG.

# Technical

* Formats:

    * We prefer .ai (source) and .svg files via Illustrator.

    * We can accept .psd (Photoshop) files and convert to Illustrator on our end. If using Photoshop, **please send a test file** early in the review stages so we can make sure the Illustrator conversion still looks reasonably the same.

* Size:

    * For image navigation:

        * SVG is vector-based and will scale to whatever size we want so there is no actual pixel widths applicable.

    * If images will be used for a publication:

        * Figure should fit on a 8.5 x 11 inch page. Depending on what is being illustrated, this can be 10.5-11 inches wide. For widths in pixels, this generally results in pixel widths of 3400 to almost 5000 pixels wide

        * Resolution should be 300 dpi

* Use logical names for artboards and use the [Anatomy ID](https://www.atlas-d2k.org/chaise/recordset/#2/Vocabulary:Anatomy/*::facets::N4IghgdgJiBcDaoDOB7ArgJwMYFM4gDkwBbPAGhCwAsUBLXJOeEAIwBswoocMQKAhDlx4gAugF8yydNhwBrHAE98SHGGxUAtCxQAPPiFXrqTVkO68JEoA@sort(RID)) for layers/groups that represent the colored anatomical regions (more on that below).

* Naming convention:

    * All lowercase - no spaces or special characters except for dashes or underscores.

    * Use underscores within phrases (ie, *mus_musculus*) and dashes between name categories (see the example below)

    * Files:

        * Include the species name at the beginning and the age stage at the end of filenames. In between, include the top-level anatomical region being illustrated in the file.

        * **<species_name>-****_<anatomy_name>_****-****<stage>**

        * Example: If you are illustrating the metanephros, use the following name (italics are the parts of the filename that will be unique): **mus_musculus-****_metanephros_****-ts28.ai
**

    * Layers/Groups -  For each active (in color) version of an anatomical region:

        * Use the [Anatomy ID (EMAPA:xxxx)](https://www.atlas-d2k.org/chaise/recordset/#2/Vocabulary:Anatomy/*::facets::N4IghgdgJiBcDaoDOB7ArgJwMYFM4gDkwBbPAGhCwAsUBLXJOeEAIwBswoocMQKAhDlx4gAugF8yydNhwBrHAE98SHGGxUAtCxQAPPiFXrqTVkO68JEoA@sort(RID)) at the beginning of the name of the layer or group. Note the IDs should be included on the work order spreadsheet.

        * For this same group/layer, please add an image map via Attributes (use the "Polygon" shape) and set the URL to a hashtag (#).

        * Example: If you are illustrating the metanephros of the kidney in one file, where the "cap mesenchyme" region is represented, create a group around the relevant layers of the active version and begin the name with: **EMAPA:27621** (After the idea, you can add a space and then add the name to help make it easier to identify which region it represents).
