---
title: Color palette for annotating histological images
permalink: /docs/color-palette-for-image-annotation/
---

Todd Valerius
2020-06-02

Annotating histological images requires drawing outlines of structures on the image and adding a Class name (the anatomical term from the approved ontology). Typically there are several examples of a given structure in an image to annotate to illustrate the various perspectives a 2D section captures of a 3D tissue structure. The same color and same anatomical name are assigned in this case. These examples are collectively merged in QuPath to collapse them into a single group annotation with a Class (Term) assigned. Next, several other structures are annotated using with the same approach with each group of like structures assigned a shared color and anatomy term after being merged. The resulting annotated image will have several sets of structures labeled and named for use. 

![Annotated BF image](https://user-images.githubusercontent.com/8427219/89831426-cdbcca80-db2b-11ea-81bd-03bb2f6a5025.png)  
_Example of an annoated histological image using the GUDMAP-defined color palette._

In QuPath, colors for Classes are randomly assigned from a broad palette in the program. I sought to identify the most useful palette of colors for use in labeling histological images and applied the following 4 criteria:

- Maximally distant colors
- Accessibility measures: account for colorblind users
- Avoid collisions with digitally restrained images
- Colors can be seem on BF H&E and IF images

I started with a set of 64 max distance colors algorithmically derived for use in data figures ([blog post - (Tatarize, 2012)](http://godsnotwheregodsnot.blogspot.com/2012/09/color-distribution-methodology.html)). This panel was examined on a colorblind simulator and problematic colors removed from that set manually ([tool - "Coblis — Color blindness simulator – Colblindor"](https://www.color-blindness.com/coblis-color-blindness-simulator/)). Since the goal here is to annotate histological images, emerging techniques that "digitally re-stain" images were considered to removed incompatible colors (an example is presented in [Kather et al. 2015](https://doi.org/10.1371/journal.pone.0145572). Finally, colors close to the common H&E colors were tested for viewability and those that are difficult to see where removed. 

This resulted in a list of 26 colors to use on H&E images that should also be compatible with most IF images. 
![Annotation Color Palette](https://user-images.githubusercontent.com/8427219/89831516-fcd33c00-db2b-11ea-85c4-a7e8cbaaab2e.png)  
_Image that includes the colors and the hex IDs for each._

The hex codes in text format:  
`"#D5FF00", "#00FF00", "#FF937E", "#91D0CB", "#0000FF", "#00AE7E", "#FF00F6", "#5FAD4E", "#01D0FF", "#BB8800", "#BDC6FF", "#008F9C", "#A5FFD2", "#FFA6FE", "#FFDB66", "#00FFC6", "#00B917", "#BDD393", "#004754", "#010067", "#0E4CA1", "#005F39", "#6B6882", "#683D3B", "#43002C", "#788231"`

### References

Coblis — Color blindness simulator – Colblindor. (n.d.). Retrieved from https://www.color-blindness.com/coblis-color-blindness-simulator/

Kather JN, Weis C-A, Marx A, Schuster AK, Schad LR, Zöllner FG (2015) New Colors for Histology: Optimized Bivariate Color Maps Increase Perceptual Contrast in Histological Images. PLoS One 10:  PMCID: PMC4696851 https://doi.org/10.1371/journal.pone.0145572

Tatarize. (2012, September 6). Color distribution methodology. Retrieved from https://godsnotwheregodsnot.blogspot.com/2012/09/color-distribution-methodology.html
