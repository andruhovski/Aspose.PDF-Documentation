---
title: Add Digital Signature to PDF file
type: docs
weight: 30
url: /java/add-digital-signature-to-pdf-file/
keywords: how to add signature to pdf using java,add digital signature to pdf using java,how to digitally signed pdf using java
Description: digitally sign PDF documents using Java. Verify, or validate the digitally sign PDFs using Java Swing or any Java-based application with Java PDF Library.
---

{{% alert color="primary" %}} 

Aspose.PDF for Java makes it possible to digitally sign PDF files using the PdfFileSignature class. You can certify a PDF file with a PKCS1-Certificate.

{{% /alert %}} 

When signing a PDF document using a signature, you basically confirm that its contents should remain "as is". Consequently, any changes made afterwards invalidate the signature and thus, you know if the document has been altered. Certifying a document first, allows you to specify the changes that a user can make to the document without invalidating the certification.

In other words, the document would still be considered to retain its integrity and the recipient could still trust the document. For further details, please visit Certifying and signing a PDF.

To accomplish the above stated requirement, the following public API changes have been made.

- isCertified(...) method is added to PdfFileSignature class.

{{< gist "aspose-pdf" "474c352a71ac9477aa0d604fd32e1c6a" "Examples-src-main-java-com-aspose-pdf-examples-NewDocumentObject-securityandsignatures-AddDigitalSignatureToPDFFile-.java" >}}
