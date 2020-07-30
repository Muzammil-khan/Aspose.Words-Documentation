---
title: Print a Document Programmatically or Using Dialogs
type: docs
weight: 50
url: /java/print-a-document-programmatically-or-using-dialogs/
---

This article describes how to print a word processing document using Aspose.Words API. It also demonstrates the methods of printing a document with Settings, Print Preview, and Print progress dialogs.
## **Printing a Document with Settings and Print Preview Dialogs**
When working with documents, it is often required to print them to a selected printer. It is helpful to utilize a print preview dialog to visually inspect how the printed document will appear and choose relevant print options.

The Aspose.Words has no built-in dialogs or forms but implements the [AsposeWordsPrintDocument](https://apireference.aspose.com/words/java/com.aspose.words/AsposeWordsPrintDocument) class overrides both java.awt.print.Printable and java.awt.print.Pageable.

The following example shows how to use these classes to print a document from Aspose.Words via the Print preview and Settings dialogs:

{{< gist "aspose-com-gists" "aa75ee5112aca57022c741270ff8cbc4" "Examples-src-main-java-com-aspose-words-examples-rendering_printing-DocumentPreviewAndPrint-PrintDialog.java" >}}

{{% alert color="primary" %}} You can download an example of using the **PrintPreviewDialog** class from [Aspose.Words GitHub](https://github.com/aspose-words/Aspose.Words-for-Java/blob/master/Examples/src/main/java/com/aspose/words/examples/rendering_printing/PrintPreviewDialog.java). {{% /alert %}} 
## **Printing Multiple Pages on One Sheet**
Aspose.Words implements the **MultipagePrintDocument** class, to fine-tune the printing operation to implement your custom logic by defining the way the document will appear on the printed page. The **MultipagePrintDocument** class provides the ability to print several pages on one sheet of paper.

{{< gist "aspose-com-gists" "aa75ee5112aca57022c741270ff8cbc4" "Examples-src-main-java-com-aspose-words-examples-rendering_printing-MultiplePagesOnSheet-MultiplePagesOnSheet.java" >}}

You can download an example of using the **MultipagePrintDocument** class from [Aspose.Words GitHub](https://github.com/aspose-words/Aspose.Words-for-Java/blob/master/Examples/src/main/java/com/aspose/words/examples/rendering_printing/MultipagePrintDocument.java). 


The result of this code example is shown below:

![todo:image_alt_text](/download/attachments/101122567/912869423)