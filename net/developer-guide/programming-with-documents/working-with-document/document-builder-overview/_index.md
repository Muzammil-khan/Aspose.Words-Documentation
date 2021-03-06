---
title: Document Builder Overview
type: docs
weight: 10
url: /net/document-builder-overview/
---

[DocumentBuilder](http://www.aspose.com/api/net/words/aspose.words/documentbuilder) is a powerful class that is associated with a [Document](http://www.aspose.com/api/net/words/aspose.words/document) and allows dynamic document building from scratch or the addition of new elements to an existing document. It provides methods to insert text, checkbox, ole object, paragraphs, lists, tables, images and other contents, specification of font, paragraph, and section formatting, and other things. Using [DocumentBuilder](http://www.aspose.com/api/net/words/aspose.words/documentbuilder) is somewhat similar in concept to using the **StringBuilder** class of the .NET Framework.

[DocumentBuilder](http://www.aspose.com/api/net/words/aspose.words/documentbuilder) complements classes and methods available in the Aspose.Words Document Object Model by simplifying most common document building tasks, such as inserting text, checkbox, ole object, tables, fields and hyperlinks.

Everything that is possible with [DocumentBuilder](http://www.aspose.com/api/net/words/aspose.words/documentbuilder) is also possible when using the classes of the Aspose.Words Document Object Model directly, but using Aspose.Words DOM classes directly usually require more lines of code than using [DocumentBuilder](http://www.aspose.com/api/net/words/aspose.words/documentbuilder).

[DocumentBuilder](http://www.aspose.com/api/net/words/aspose.words/documentbuilder) has an internal cursor that you can navigate to a different location in a document using various **DocumentBuilder.MoveToXXX** methods such as [DocumentBuilder.MoveToDocumentStart](http://www.aspose.com/api/net/words/aspose.words/documentbuilder/methods/movetodocumentstart) and [DocumentBuilder.MoveToField](http://www.aspose.com/api/net/words/aspose.words/documentbuilder/methods/movetofield) .

You can insert text, checkbox, ole object, images, bookmarks, form fields, and other document elements at the cursor position using any of **DocumentBuilder.InsertXXX** methods such as [DocumentBuilder.InsertField](http://www.aspose.com/api/net/words/aspose.words.documentbuilder/insertfield/methods/1) , [DocumentBuilder.InsertHtml](http://www.aspose.com/api/net/words/aspose.words/documentbuilder/methods/inserthtml) and other similar methods.

Aspose.Words API provides several classes responsible for different document elements’ formatting. Each of the classes encapsulates a number of formatting properties related to a particular document element such as text, paragraph, section, and so on. For example, the [Font](http://www.aspose.com/api/net/words/aspose.words/font) class represents character formatting properties, the [ParagraphFormat](http://www.aspose.com/api/net/words/aspose.words/paragraphformat) class represents paragraph formatting properties etc. The objects of these classes are returned by the corresponding **DocumentBuilder** properties (that have the same names as the classes) so you can access them and set the desired formatting during the document build.

To start, you need to create a **DocumentBuilder** and associate it with a **Document** object. Create a new instance of [DocumentBuilder](http://www.aspose.com/api/net/words/aspose.words/documentbuilder) by calling its constructor and pass to it a [Document](http://www.aspose.com/api/net/words/aspose.words/document) object for attachment to the builder. To insert a text, simply pass the string of text you need to insert into the document to the [DocumentBuilder.Write](http://www.aspose.com/api/net/words/aspose.words/documentbuilder/methods/write) method. Below example shows how to create a simple document using a document builder.

{{< gist "aspose-com-gists" "0b968ac8900f80c11e109dffb105f3da" "Examples-CSharp-Programming-Documents-Comments-AddComments-CreateSimpleDocumentUsingDocumentBuilder.cs" >}}

Text formatting is determined by the Font property. This object contains different font attributes (font name, font size, color, and so on). Some important font attributes are also represented by [DocumentBuilder](http://www.aspose.com/api/net/words/aspose.words/documentbuilder) properties to allow you to access them directly. These are Boolean properties [Font.Bold](http://www.aspose.com/api/net/words/aspose.words/font/properties/bold), [Font.Italic](http://www.aspose.com/api/net/words/aspose.words/font/properties/italic), and [Font.Underline](http://www.aspose.com/api/net/words/aspose.words/font/properties/underline). Below example Inserts formatted text using DocumentBuilder:

{{< gist "aspose-com-gists" "0b968ac8900f80c11e109dffb105f3da" "Examples-CSharp-Programming-Documents-Document-WriteAndFont-WriteAndFont.cs" >}}

{{% alert color="primary" %}} 

Note that the character formatting you set will apply to all text inserted from the current position in the document onwards.

{{% /alert %}}
