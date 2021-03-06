---
title: Creating or Loading a Document
type: docs
weight: 10
url: /net/creating-or-loading-a-document/
---

Almost any task that you want to perform with Aspose.Words involves loading a document. The Document class represents a document loaded into memory. The document has several overloaded constructors allowing you to create a blank document or to load it from a file or stream. The document can be loaded in any load format supported by Aspose.Words. For the list of all supported load formats, see the [LoadFormat](https://apireference.aspose.com/net/words/aspose.words/loadformat) enumeration.
## **Create a New Document**
We will call the [Document](https://apireference.aspose.com/net/words/aspose.words/document/constructors/main) constructor without parameters to create a new blank document. If you want to generate a document programmatically, the simplest way is to use the [DocumentBuilder](https://apireference.aspose.com/net/words/aspose.words/documentbuilder) class to add document contents.

The following code example shows how to create a document using the document builder:

{{< gist "aspose-com-gists" "0b968ac8900f80c11e109dffb105f3da" "Examples-CSharp-Loading-and-Saving-CreateDocument-CreateDocument.cs" >}}

{{% alert color="primary" %}} 

Note the default values:

- A blank document contains one section with default parameters, one empty paragraph, some document styles. Actually this document is the same as the result of creating the “New document” in Microsoft Word.
- The document paper size is [PaperSize](https://apireference.aspose.com/words/net/aspose.words/papersize).**Letter**.

{{% /alert %}} 
## **Load a Document**
To load an existing document in any of the [LoadFormat](https://apireference.aspose.com/net/words/aspose.words/loadformat) formats, pass the file name or the stream into one of the Document constructors. The format of the loaded document is automatically determined by its extension.
### **Load from a File**
Pass a file name as string to the Document constructor to open an existing document from a file.

The following code example shows how to open a document from a file:

{{< gist "aspose-com-gists" "0b968ac8900f80c11e109dffb105f3da" "Examples-CSharp-Loading-and-Saving-LoadAndSaveToDisk-OpenDocument.cs" >}}

You can download the template file of this example from [Aspose.Words GitHub](https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Quick-Start/Document.doc).
### **Load from a Stream**
To open a document from a stream, simply pass a stream object that contains the document into the Document constructor.

The following code example shows how to open a document from a stream:

{{< gist "aspose-com-gists" "0b968ac8900f80c11e109dffb105f3da" "Examples-CSharp-Loading-and-Saving-LoadAndSaveToStream-OpeningFromStream.cs" >}}

{{% alert color="primary" %}} 

You can download the template file of this example from [Aspose.Words GitHub](https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Quick-Start/Document.doc).

{{% /alert %}}
