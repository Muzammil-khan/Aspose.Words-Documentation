---
title: Section Features Supported on Rich Text Import
type: docs
weight: 100
url: /net/section-features-supported-on-rich-text-import/
---

{{% alert color="primary" %}} 

Sections allow you to divide parts of the document so page formatting and headers and footers apply only to that part of the document. This allows for example different parts of the document to completley different page sizes or page orientations.

A section is represented as a Section node in the Aspose.Words model.

Aspose.Words supports the creation and deletion of sections in a document, along with accessing and modifying all section properties.

See the following links in the documentation for further information:

- [Section](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.section.html)
- [Document.Sections](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.document.sections.html)

[Jump to this location in the export section](/pages/createpage.action?spaceKey=wordsnet&title=Rtf+Export&linkCreation=true&fromPageId=2595795)

{{% /alert %}} 
##### **Headers and Footers**
Each Header and Footer in a document is stored per section. Each header or footer is imported into Aspose.Words as a HeaderFooter node. This node is always a child of a Section. 

Most documents have header or footer content represented by the primary header or footer. This displays content on all pages of the section. There is also different types of headers and footers to display different content on the first page or even/odd pages of the header footer.

There can be up to three different types of headers and three different types of footers per section. You can only have one type of the header or footer per section.

In Aspose.Words this is represented by Header Footer nodes of different types. The different types are:

- HeaderFirst
- HeaderPrimary
- HeaderEven
- FooterFirst
- FooterPrimary
- FooterEven

See the following links in the documentation for further information:

- [Section.HeadersFooters](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.section.headersfooters.html)
- [PageSetup.DifferentFirstPageHeaderFooter](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.pagesetup.differentfirstpageheaderfooter.html)
- **PageSetup.OddAndEvenPageHeaderFooter**
- [HeaderFooterCollection.LinkToPrevious](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.headerfootercollection.linktoprevious overloads.html)

|**Feature**|**Supported**|**Comment**|**See Also**|
| :- | :- | :- | :- |
|Different First Page |Yes | | |
|Different Even and Odd Pages |Yes |Note that setting a Microsoft Word Document to display even or odd header footers applies to the entire document. If you set this option in Microsoft Word then all sections follow this rule. Even though this is a documentw-wide setting, in Aspose.Words this property appears per section as a PageSetup property. Changing this property affects all sections in the document. | |
|Continue from Previous Section |Yes |<p>In a Microsoft Word document a header or footer can be linked to the previous section. This means the same headers and footers from the section before will be displayed for this section as well. In some cases you can check this by using the HeaderFooter.LinkedToPrevious property. <br><br>In Aspose.Words, the different situations are represented in the model as follows: </p><p>- If a document has no headers or footers of a certain type then no Section node contains any child Header Footer of that type. </p><p>- If header or footer is not linked to the previous section (the header of footer is different from the previous section) then the Section node will have its own Header Footer node of that type. This is the same for each type of header or footer that is not linked in the Section. </p><p>- If a header or footer is linked to the previous section then there will be no header or footer of that type in the current section. This means that a section that appears to have no header or footer nodes can still be displaying headers and footers as they come from previous sections. Check the HeaderFooter.LinkedToPrevious property. </p><p>- If a header or footer is not linked to the previous section but it simply blank (no content) then there will be a header or footer in that section, however it will contain no content (no runs). <br><br>  You can link/unlink header footers from previous sections by using the HeaderFooter.LinkToPrevious method. If you unlink a headerfooter from the previous section using Microsoft Word, the content from the previous header or footer is copied over. In Aspose.Words however the header footer is unlinked but left blank. You can copy the content from the previous section if required. Note that you can choose to unlink all headers and footers of all types or just a particular type. For example the primary header footer can be different whereas the primary footer can still be linked to the previous section. </p>| |
##### **Section Break Type**
See the following links in the documentation for further information:

- [PageSetup.SectionStart](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.pagesetup.sectionstart.html)
- [DocumentBuilder.InsertBreak](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.documentbuilder.insertbreak.html)

|**Feature**|**Supported**|**Comment**|**See Also**|
| :- | :- | :- | :- |
|Continuous |Yes | | |
|Even Page |Yes | | |
|Odd Page |Yes | | |
|Next Column |Yes | | |
|Next Page |Yes | | |
##### **Text Columns**
See the following link in the documentation for further information:

- [PageSetup.TextColumns](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.pagesetup.textcolumns.html)

|**Feature**|**Supported**|**Comment**|**See Also**|
| :- | :- | :- | :- |
|Text Columns |Yes | | |
##### **Page Margins**
See the following links in the documentation for further information:

- [PageSetup](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.pagesetup.html)
- [PageSetup.LeftMargin](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.pagesetup.leftmargin.html)
- [PageSetup.FooterDistance](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.pagesetup.footerdistance.html)
- [PageSetup.Gutter](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.pagesetup.gutter.html)

|**Feature**|**Supported**|**Comment**|**See Also**|
| :- | :- | :- | :- |
|Page Margins |Yes | | |
##### **Page Numbering**
See the following links in the documentation for further information:

- **PageSetup.PageNumberingStyle**
- [PageSetup.PageStartingNumber](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.pagesetup.pagestartingnumber.html)
- [PageSetup.RestartPageNumbering](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.pagesetup.restartpagenumbering.html)

|**Feature**|**Supported**|**Comment**|**See Also**|
| :- | :- | :- | :- |
|Page Numbering |Yes | | |
##### **General Formatting**

|**Feature**|**Supported**|**Comment**|**See Also**|
| :- | :- | :- | :- |
|Right to Left Section |Yes | |- [PageSetup.Bidi](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.pagesetup.bidi.html)|
|Line Numbering |Yes | |<p>- [PageSetup.LineNumberCountBy](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.pagesetup.linenumbercountby.html) </p><p>- [PageSetup.LineNumberDistanceFromText](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.pagesetup.linenumberdistancefromtext.html) </p><p>- [PageSetup.LineNumberRestartMode](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.pagesetup.linenumberrestartmode.html) </p><p>- [PageSetup.LineStartingNumber](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.pagesetup.linestartingnumber.html)</p>|
|Paper Source |Yes | |<p>- [PageSetup.FirstPageTray](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.pagesetup.firstpagetray.html) </p><p>- **PageSetup.OtherPageTray**</p>|
|Paper Size |Yes | |- [PageSetup.PaperSize](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.pagesetup.papersize.html)|
|Orientation |Yes | |- [PageSetup.Orientation](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.pagesetup.orientation.html)|
|Protection |Yes | |- **Section.ProtectedForForms**|
|Text Direction |Yes | | |
|Vertical Alignment |Yes | |- [PageSetup.VerticalAlignment](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.pagesetup.verticalalignment.html)|
|Asian Document Grid |Yes | | |
##### **Chapter Numbering**

|**Feature**|**Supported**|**Comment**|**See Also**|
| :- | :- | :- | :- |
|Chapter Numbering |Yes | | |
##### **Page Border**
See the following links in the documentation for further information:

- [PageSetup.Borders](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.pagesetup.borders.html)
- **PageSetup.PageBorderAppliesTo**
- **PageSetup.BordersAlwaysInFront**
- **PageSetup.BordersSurroundsHeader**

|**Feature**|**Supported**|**Comment**|**See Also**|
| :- | :- | :- | :- |
|Page Border |Yes | | |
