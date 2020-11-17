---
title: Extract and save an attachment 
type: docs
weight: 40
url: /net/extract-and-save-an-attachment/
---
# Extract and save an attachment 
With Aspose.PDF, it is possible to get all attachments from a PDF document. This is useful either when you want to save the documents separately from the PDF, or if you need to strip a PDF of attachments.

To get all attachments from a PDF file:

1. Loop through the [Document](https://apireference.aspose.com/pdf/net/aspose.pdf/document) object’s [EmbeddedFiles](https://apireference.aspose.com/pdf/net/aspose.pdf/embeddedfilecollection) collection. The [EmbeddedFiles](https://apireference.aspose.com/pdf/net/aspose.pdf/embeddedfilecollection) collection contains all attachments. Each element of this collection represents a [FileSpecification](https://apireference.aspose.com/pdf/net/aspose.pdf/filespecification) object. Each iteration of the foreach loop through the [EmbeddedFiles](https://apireference.aspose.com/pdf/net/aspose.pdf/embeddedfilecollection) collection returns a [FileSpecification](https://apireference.aspose.com/pdf/net/aspose.pdf/filespecification) object.
1. Once the object is available, retrieve either all the attached file’s properties or the file itself.

The following code snippets show how to get all the attachments from a PDF document.
```cshrap
// For complete examples and data files, please go to https://github.com/aspose-pdf/Aspose.PDF-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_AsposePdf_Attachments();

// Open document
Document pdfDocument = new Document(dataDir + "GetAlltheAttachments.pdf");
            
// Get embedded files collection
EmbeddedFileCollection embeddedFiles = pdfDocument.EmbeddedFiles;
            
// Get count of the embedded files
Console.WriteLine("Total files : {0}", embeddedFiles.Count);

int count = 1;
            
// Loop through the collection to get all the attachments
foreach (FileSpecification fileSpecification in embeddedFiles)
{
    Console.WriteLine("Name: {0}", fileSpecification.Name);
    Console.WriteLine("Description: {0}",
    fileSpecification.Description);
    Console.WriteLine("Mime Type: {0}", fileSpecification.MIMEType);

    
    
    // Check if parameter object contains the parameters
    if (fileSpecification.Params != null)
    {
        Console.WriteLine("CheckSum: {0}",
        fileSpecification.Params.CheckSum);
        Console.WriteLine("Creation Date: {0}",
        fileSpecification.Params.CreationDate);
        Console.WriteLine("Modification Date: {0}",
        fileSpecification.Params.ModDate);
        Console.WriteLine("Size: {0}", fileSpecification.Params.Size);
    }
    
    // Get the attachment and write to file or stream
    byte[] fileContent = new byte[fileSpecification.Contents.Length];
    fileSpecification.Contents.Read(fileContent, 0,
    fileContent.Length);
    FileStream fileStream = new FileStream(dataDir + count + "_out" + ".txt",
    FileMode.Create);
    fileStream.Write(fileContent, 0, fileContent.Length);
    fileStream.Close();
    count+=1;
}
```
Get Individual Attachment
In order to get an individual attachment, we can specify the index of attachment in *EmbeddedFiles* object of Document instance. Please try using following code snippet.

C#
```
// For complete examples and data files, please go to https://github.com/aspose-pdf/Aspose.PDF-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_AsposePdf_Attachments();

// Open document
Document pdfDocument = new Document(dataDir + "GetIndividualAttachment.pdf");

// Get particular embedded file
FileSpecification fileSpecification = pdfDocument.EmbeddedFiles[1];
            
// Get the file properties
Console.WriteLine("Name: {0}", fileSpecification.Name);
Console.WriteLine("Description: {0}", fileSpecification.Description);
Console.WriteLine("Mime Type: {0}", fileSpecification.MIMEType);
            
// Check if parameter object contains the parameters
if (fileSpecification.Params != null)
{
    Console.WriteLine("CheckSum: {0}",
    fileSpecification.Params.CheckSum);
    Console.WriteLine("Creation Date: {0}",
    fileSpecification.Params.CreationDate);
    Console.WriteLine("Modification Date: {0}",
    fileSpecification.Params.ModDate);
    Console.WriteLine("Size: {0}", fileSpecification.Params.Size);
}

            
// Get the attachment and write to file or stream
byte[] fileContent = new byte[fileSpecification.Contents.Length];
fileSpecification.Contents.Read(fileContent, 0, fileContent.Length);

FileStream fileStream = new FileStream(dataDir + "test_out" + ".txt", FileMode.Create);
fileStream.Write(fileContent, 0, fileContent.Length);
fileStream.Close();
```
