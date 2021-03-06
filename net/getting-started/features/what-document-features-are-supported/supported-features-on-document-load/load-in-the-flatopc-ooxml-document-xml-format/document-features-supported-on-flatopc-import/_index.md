---
title: Document Features Supported on FlatOPC Import
type: docs
weight: 30
url: /net/document-features-supported-on-flatopc-import/
---

{{% alert color="primary" %}} 

Office Open XML (OOXML) is the new XML-based format introduced in Microsoft Office 2007 applications. Office Open XML is a container format for several specialized XML-based markup languages. WordprocessingML is the markup language used by Microsoft Office Word to store its DOCX documents.

Aspose.Words supports all major OOXML versions:

- Microsoft Word 2007 (OOXML ECMA-376)
- Microsoft Word 2010 (OOXML ISO/IEC DIS 29500)

OOXML WordprocessingML documents most often come as DOCX files, which are ZIP packages. In addition to DOCX, Aspose.Words also supports loading and saving OOXML in the “plain XML” Flat OPC format.

Aspose.Words provides extensive support for loading, saving and converting WordprocessingML documents.

See the following links in the documentation for further information:

- [Loading, Saving and Converting](/words/net/loading-2c-saving-and-converting-html/)
- [Working with Document old](/pages/createpage.action?spaceKey=wordsnet&title=Working+with+Document+old&linkCreation=true&fromPageId=2596110)
- [Aspose.Words Document Object Model](/words/net/aspose-words-document-object-model-html/)
- [Document](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.document.html)

{{% /alert %}} 
## **General**

|**Feature**|**Supported**|**Comment**|**See Also**|
| :- | :- | :- | :- |
|Attached Template|Yes|Attached template is used to reference styles and other settings through the use of a separate document template. <br><br>The link to this template is imported from the source document and can be found in the API as the Document.AttachedTemplate property.|- [Document.AttachedTemplate](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.document.attachedtemplate.html)|
|Built-In Properties|Yes|All Built-in Document Properties can be accessed and modified in Aspose.Words API. <br><br>There are methods to update the "count" properties such as character, word and page count. All such properties are supported with the exception of the "line" count which is currently not updated.|<p>- [Document.BuiltInDocumentProperties](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.document.builtindocumentproperties.html)</p><p>- [Document.UpdatePageLayout](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.document.updatepagelayout.html)</p><p>- [Document.UpdateWordCount](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.document.updatewordcount.html)</p>|
|Custom Properties|Yes|Custom Document Properties can be created, accessed and modified through the API.|- [Document.CustomDocumentProperties](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.document.customdocumentproperties.html)|
|Custom Payload Part|Yes|Only Custom Payload Parts that are attached to the root of the package are preserved on load. <br><br>Custom Parts can be accessed through the Aspose.Words API.|- [Document.PackageCustomParts](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.document.packagecustomparts.html)|
|Custom XML Data Storage|Yes|Custom XML Parts can be accessed and modified in the DOM. <br><br>You can remove schemas linked to a part, however you cannot schemas in the document that are not referenced. <br><br>This feature will be supported in a future version.|- [Document.CustomXmlParts](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.document.customxmlparts.html)|
|Digital Signature|Yes|A digital signature ensures that the content of a document has not been tampered with during transit. A signature is applied over the document so if any part of it is modified the signature is invalidated. <br><br>When you load a document into Aspose.Words the document signature is automatically lost. This is by design as the document is not the same anymore. You will need to reapply another signature during export, however currently Aspose.Words only signs PDF documents on output. <br><br>There are plans to support signing documents on export when saving in the OOXML, DOC, ODT or XPS format. <br><br>Detection, access and verification of digital signatures is supported. <br><br>Signing a OOXML document is not yet supported.|<p>- [Working with Digital Signatures](/words/net/working-with-digital-signatures-html/)</p><p>- **Document.DigitalSigntures**</p><p>- [DigitalSignatureCollection.IsValid](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.digitalsignaturecollection.isvalid.html)</p>|
|Embedded Package|Yes|<p>Embedded packages are generally supported by Aspose.Words. There are two ways documents can be embedded inside other documents:</p><p>- OLE (this is available in DOC and OOXML formats)</p><p>- Package Embedding (available in OOXML only) <br><br>  Content can be extracted from both types of embedded packages by using the OleFormat.Save method. <br><br>  Aspose.Words supports these in the following ways during conversion: <br><br>  If you have an OLE embedded or linked object it will be preserved during any conversion (e.g. DOC to DOCX or DOCX to DOC etc). <br><br>  If you have a Package Embedded document, then it will only be preserved during DOCX to DOCX conversion. <br><br>  There is no way to save a Package Embedded document from DOCX into a DOC file without converting it into an OLE embedded object. Implementing conversion of Package Embedded to OLE is tricky and it will take a while to implement. <br><br>  OLE objects contain "native data" and are supposed to be created by the actual OLE creating application. We at Aspose.Words have never attempted or planned to replace the behavior of OLE creating applications.</p>|- [Shape.OleFormat](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.drawing.shape.oleformat.html)|
|Encryption|Yes|Encrypted documents can be loaded into Aspose.Words as long as the password supplied on load for the document is correct. <br><br>XOR obfuscation is currently unsupported. <br><br>Encrypting a document during save is currently unsupported with the exception when saving in DOC format. <br><br>Opening documents encrypted using the ECMA-376 Standard Encryption or Agile Encryption is supported <br><br>Opening documents encrypted using the Extensible Encryption is not supported.|<p>- [LoadOptions.Password](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.loadoptions.password.html)</p><p>- [FileFormatInfo.IsEncrypted](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.fileformatinfo.isencrypted.html)</p>|
|Font Table|Yes| | |
|Glossary Document/Quick Parts/Auto Text|Yes|Glossary Document for DOCX is accessiable through the DOM.|- [Document.GlossaryDocument](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.document.glossarydocument.html)|
|Hyphenation|Yes|There is currently no API to access and modify hypenation settings in a document.|- [ParagraphFormat.SuppressAutoHyphens](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.suppressautohyphens.html)|
|Key Map Customizations|Yes| | |
|Mail Merge Recipient Data|Yes| |- [Document.MailMergeSettings](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.document.mailmergesettings.html)|
|Office Math|Yes|Office math content is accessable through the DOM.|- [OfficeMath](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.math.officemath.html)|
|Themes|Yes|There is currently no API to access information about Themes however they are preserved when exporting to most formats. <br><br>Themes are preserved during open/save cycle.| |
|Toolbar Customizations|Yes| | |
|Variables|Yes|Variables allow you to store additional information in the document which is "hidden" from the main document. <br><br>This can be used to embed custom tracking data in the document itself.|- [Document.Variables](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.document.variables.html)|
|VBA Project (Macro)|Yes|VBA Projects are preserved during open and save to different formats that support them. This means you can load an existing template/document and add content to it and the VBA Projects will remain properly. <br><br>There is no API to access the code behind or execute any of the macros. There is a method provided to remove all macros from a document.|- [Document.RemoveMacros](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.document.removemacros.html)|
|VBA Project Digital Signature|Yes|The digital signature on a VBA Project is preserved during open and save even if the document content is modified.| |
|Background|Yes|A background of a Word document can be a solid color or an image.|- [Document.BackgroundShape](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.documentbase.backgroundshape.html)|
|Thumbnail|Planned| |- [BuiltInDocumentProperties.Thumbnail](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.properties.builtindocumentproperties.thumbnail.html)|
## **Embedded Fonts**

|**Feature**|**Supported**|**Comment**|**See Also**|
| :- | :- | :- | :- |
|Embed Fonts|Planned|Currently embedding new fonts into a document is unsupported.| |
|Access and Use Embedded Fonts|Yes|Embedded fonts in DOCX are preserved and can be accessed through the API.|<p>- [FontInfo](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.fonts.fontinfo.html)</p><p>- [FontInfo.GetEmbeddedFont](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.fonts.fontinfo.getembeddedfont.html)</p>|
## **Bibliography**

|**Feature**|**Supported**|**Comment**|**See Also**|
| :- | :- | :- | :- |
|Bibliography|Yes|Bibliography content is preserved on import. <br><br>Updating a bibliography is currently unsupported.| |
|Sources/Citations|Yes|Sources and citations are preserved during import. <br><br>Inserting new sources is not supported.| |
|Citation Style|Yes|Document-wide citation style is preserved but there is no access to this setting in the DOM.| |
## **Protection**
Aspose.Words supports most document protection features. Using Aspose.Words you can open a document that is password protected even without the password (as long as its not encrypted).

Once loaded you can remove any protection from a document.

See the following links in the documentation for further information:

- [Protecting Documents](/words/net/working-with-document/#workingwithdocument-protectingdocuments)
- [Document.Protect](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.document.protect overloads.html)
- [Document.Unprotect](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.document.unprotect overload 1.html)

|**Feature**|**Supported**|**Comment**|**See Also**|
| :- | :- | :- | :- |
|Allow Only Comments|Yes| |- [Document.ProtectionType](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.document.protectiontype.html)|
|Allow Only Form Fields|Yes| |- **Document.ProtectionType**|
|Allow Only Revisions|Yes|When this protection type is enabled, tracked changes are automatically turned on.|<p>- **Document.ProtectionType**</p><p>- **Document.TrackChanges**</p>|
|Limit Formatting to Selection of Styles|Yes|This setting is retained during round-trip. There is currently no way to modify these settings in the API.| |
|Protection Password (Legacy)|Yes| |- [WriteProtection.SetPassword](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.settings.writeprotection.setpassword.html)|
|Protection Password (OOXML)|Yes| |- **WriteProtection.SetPassword**|
|Protected Sections|Yes| |- [Section.ProtectedForForms](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.section.protectedforforms.html)|
|Protection Ranges|Planned|Currently protected ranges are lost upon import.| |
|Read Only|Yes| |<p>- [Document.WriteProtection](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.document.writeprotection.html)</p><p>- [WriteProtection.IsWriteProtected](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.settings.writeprotection.iswriteprotected.html)</p>|
## **Settings**

|**Feature**|**Supported**|**Comment**|**See Also**|
| :- | :- | :- | :- |
|Asian Typography Settings|Yes| | |
|Compatibility Options|Yes| |- [Document.CompatibilityOptions](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.document.compatibilityoptions.html)|
|Endnote Options|Yes| |- [Document.EndnoteOptions](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.document.endnoteoptions.html)|
|Footnote Options|Yes| |- [Document.FootnoteOptions](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.document.footnoteoptions.html)|
|Mail Merge Settings|Yes|You can modify all mail merge settings, as well as setting a new mail merge data source for the document to use.|- **Document.MailMergeSettings**|
|Print Settings|Yes| |- [Section.PageSetup](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.section.pagesetup.html)|
|Show/Hide Settings|Yes| | |
|View Settings|Yes| |- [Document.ViewOptions](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.document.viewoptions.html)|
|Web Settings|Yes| | |
|XML Settings|Yes| | |

