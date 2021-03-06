---
title: Remove tables from existing PDF
type: docs
weight: 40
url: /java/remove-tables-from-existing-pdf/
---

{{% alert color="primary" %}}

Aspose.PDF for Java offers the capabilities to insert/create Table inside PDF document while its being generated from scratch or you can also add the table object in any existing PDF document. However you may have a requirement to [Manipulate Tables in existing PDF](https://docs.aspose.com/pdf/java/manipulate-tables-in-existing-pdf/) where you can update the contents in existing table cells. However you may come across a requirement to remove table objects from existing PDF document.

{{% /alert %}}

In order to remove the tables, we need to use TableAbsorber class to get hold of tables in existing PDF and then replace the table cell contents with blank characters and in order to remove the border, certain page region is redacted. The following code snippet shows the steps to delete table from existing PDF document.

{{< gist "aspose-com-gists" "c0e07056c427f1c8a81336809a7ae4f2" "Examples-src-main-java-com-aspose-pdf-examples-NewDocumentObject-tables-RemoveTablesFromExistingPDF-.java" >}}
