---
title: Convert PDF to XPS
type: docs
weight: 310
url: /net/convert-pdf-to-xps/
---
# Convert PDF to XPS

The XPS file type is primarily associated with the XML Paper Specification by Microsoft Corporation. The XML Paper Specification (XPS), formerly codenamed Metro and subsuming the Next Generation Print Path (NGPP) marketing concept, is Microsoft's initiative to integrate document creation and viewing into the Windows operating system.

To convert PDF files to XPS, Aspose.PDF has the class XpsSaveOptions that is used as the second argument to the Document.Save(..) constructor to generate the XPS file. The following code snippet shows the process of converting PDF file into XPS format.

```csharp
// For complete examples and data files, please go to https://github.com/aspose-pdf/Aspose.PDF-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_AsposePdf_DocumentConversion();

// Load PDF document
Document pdfDocument = new Document(dataDir + "input.pdf");

// Instantiate XPS Save options
Aspose.Pdf.XpsSaveOptions saveOptions = new Aspose.Pdf.XpsSaveOptions();
// Save the XPS document
pdfDocument.Save("PDFToXPS_out.xps", saveOptions)
```