---
title: Crop Pages
type: docs
weight: 30
url: /net/crop-pages/
---
# Crop pages

## Get Page Properties
Each page in a PDF file has a number of properties, such as the width, height, bleed-, crop- and trimbox. Aspose.PDF allows you to access these properties.

**Understanding Page Properties: the Difference between Artbox, BleedBox, CropBox, MediaBox, TrimBox and Rect property**
-  **Media box**: The media box is the largest page box. It corresponds to the page size (for example A4, A5, US Letter, etc.) selected when the document was printed to PostScript or PDF. In other words, the media box determines the physical size of the media on which the PDF document is displayed or printed.
- **Bleed box**: If the document has bleed, the PDF will also have a bleed box. Bleed is the amount of color (or artwork) that extends beyond the edge of a page. It is used to make sure that when the document is printed and cut to size (“trimmed”), the ink will go all the way to the edge of the page. Even if the page is mistrimmed - cut slightly off the trim marks - no white edges will appear on the page.
- **Trim box**: The trim box indicates the final size of a document after printing and trimming.
- **Art box**: The art box is the box drawn around the actual contents of the pages in your documents. This page box is used when importing PDF documents in other applications.
- **Crop box**: The crop box is the “page” size at which your PDF document is displayed in Adobe Acrobat. In normal view, only the contents of the crop box are displayed in Adobe Acrobat. For detailed descriptions of these properties, read the Adobe.Pdf specification, particularly 10.10.1 Page Boundaries.
- **Page.Rect**: the intersection (commonly visible rectangle) of the MediaBox and DropBox. The picture below illustrates these properties.
For further details, please visit [this page](http://www.enfocus.com/manuals/ReferenceGuide/PP/10/enUS/en-us/concept/c_aa1095731.html).
