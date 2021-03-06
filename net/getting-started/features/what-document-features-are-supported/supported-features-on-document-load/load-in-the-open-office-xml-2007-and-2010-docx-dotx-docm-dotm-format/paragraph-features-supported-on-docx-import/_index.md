---
title: Paragraph Features Supported on DOCX Import
type: docs
weight: 90
url: /net/paragraph-features-supported-on-docx-import/
---

{{% alert color="primary" %}} 

Each paragraph in a document is represented in Aspose.Words as a Paragraph node. A paragraph represesents a block of text in a document and have a variety of properties and styles.

Using Aspose.Words you can access and change virtually all properties of a paragraph. Nearly all paragraph attributes are supported. You can also easily insert and remove paragraphs.

Paragraph formatting is contained within the ParagraphFormat class which is linked to the paragraph.

See the following links in the documentation for further information:

- [Inserting Document Elements](/pages/createpage.action?spaceKey=wordsnet&title=Inserting+Document+Elements&linkCreation=true&fromPageId=2595992)
- [Paragraph](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraph.html)
- [Paragraph.ParagraphFormat](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraph.paragraphformat.html)

[Jump to this location in the export section](/pages/createpage.action?spaceKey=wordsnet&title=Ooxml+Export&linkCreation=true&fromPageId=2595992)

{{% /alert %}} 
##### **General Formatting**

|**Feature**|**Supported**|**Comment**|**See Also**|
| :- | :- | :- | :- |
|Paragraph Style |Yes | |<p>- [ParagraphFormat](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.html) </p><p>- [ParagraphFormat.Style](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.style.html)</p>|
|Alignment |Yes |The special "Thai Distributed" alignment is also supported during conversion. There is currently no API to access or modify this alignment. |- [ParagraphFormat.Alignment](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.alignment.html)|
|Right to Left Paragraph |Yes | |- [ParagraphFormat.Bidi](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.bidi.html)|
|Bullets and Numbers |Yes | |<p>- **ParagraphFormat.ListFormat** </p><p>- **ParagraphFormat.ListLabel**</p>|
|Outline Level |Yes | |- [ParagraphFormat.OutlineLevel](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.outlinelevel.html)|
|Run Properties for the Paragraph Mark |Yes | |- **ParagraphFormat.ParagraphBreakFont**|
|Suppress Line Numbers |Yes | |- **ParagraphFormat.SurpressLineNumbers**|
|Suppress Hyphenation |Yes | |- **ParagraphFormat.SurpressAutoHyphens**|
##### **Indents**

|**Feature**|**Supported**|**Comment**|**See Also**|
| :- | :- | :- | :- |
|Left Indent |Yes | |- [ParagraphFormat.LeftIndent](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.leftindent.html)|
|Right Indent |Yes | |- [ParagraphFormat.RightIndent](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.rightindent.html)|
|First Line Indent |Yes | |- [ParagraphFormat.FirstLineIndent](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.firstlineindent.html)|
|Hanging Indent |Yes | |- **ParagraphFormat.FirstLineIndent**|
|Mirror Indents |Yes | |<p>- **ParagraphFormat.LeftIndent** </p><p>- **ParagraphFormat.RightIndent**</p>|
|Automatically Adjust Right Indent |Yes | | |
##### **Spacing**

|**Feature**|**Supported**|**Comment**|**See Also**|
| :- | :- | :- | :- |
|Space Before |Yes | |- [ParagraphFormat.SpaceBefore](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.spacebefore.html)|
|Space After |Yes | |- [ParagraphFormat.SpaceAfter](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.spaceafter.html)|
|Space Auto |Yes | |<p>- [ParagraphFormat.SpaceBeforeAuto](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.spacebeforeauto.html) </p><p>- [ParagraphFormat.SpaceAfterAuto](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.spaceafterauto.html)</p>|
|Line Spacing |Yes | |<p>- [ParagraphFormat.LineSpacing](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.linespacing.html) </p><p>- [ParagraphFormat.LineSpacingRule](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.linespacingrule.html)</p>|
|No Space between Conforming Paragraphs |Yes | |- [ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.nospacebetweenparagraphsofsamestyle.html)|
|Snap To Grid |Yes | | |
##### **Keeps and Breaks**

|**Feature**|**Supported**|**Comment**|**See Also**|
| :- | :- | :- | :- |
|Widow/Orphan Control |Yes | |- [ParagraphFormat.WidowControl](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.widowcontrol.html)|
|Keep With Next |Yes | |- [ParagraphFormat.KeepWithNext](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.keepwithnext.html)|
|Keep Lines Together |Yes | |- [ParagraphFormat.KeepTogether](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.keeptogether.html)|
|Page Break Before |Yes | |- [ParagraphFormat.PageBreakBefore](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.pagebreakbefore.html)|
##### **Text Frames**
This is the legacy text frames from Word 97, not to be confused with the Autoshape Textbox which is discussed under Drawing Objects.

Text frames are preserved in the model but there is no API or node to modify or access information about frames.

|**Feature**|**Supported**|**Comment**|**See Also**|
| :- | :- | :- | :- |
|Text Frames |Yes | | |
##### **Tab Stops**
All features of tab stops are supported in Aspose.Words except for relative tab stops.

Using Aspose.Words you can find tab stops based off position or index. You can change tab stop features like position, alignment etc or remove tabstops completely.

See the following link in the documentation for further information:

- [ParagraphFormat.TabStops](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.tabstops.html)

|**Feature**|**Supported**|**Comment**|**See Also**|
| :- | :- | :- | :- |
|Absolute Position |Yes | |- [TabStop.Position](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.tabstop.position.html)|
|Relative Position |Yes |A relative position tab can be inserted in Microsoft Word using the "Insert Alignment Tab" button. This type of tab is relative to either the page margin or the indent of the paragraph. <br><br>This allows tab stops to appear in the same relative place even when the position of the paragraph or page is modified. <br><br>Currently Aspose.Words supports these types of tab stops in OOXML and WordML formats only. There is currently no API to retrieve the properties of this tab e.g RelativeTo, Alignment, Leader etc. Further support is planned. |- [AbsolutePositionTab](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.absolutepositiontab.html)|
|Alignment: Left, Center, Right, Decimal, Bar |Yes | |- [TabStop.Alignment](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.tabstop.alignment.html)|
|Leader |Yes | |- [TabStop.Leader](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.tabstop.leader.html)|
##### **Drop Caps**
Drop Caps are partially supported and preserved during document conversion. A drop cap is a text frame which is imported as a separate paragraph (from the rest of the paragraph as seen in the source document).

You can modify drop cap properties and position, however the new settings are not applied to the drop cap. You cannot yet create new drop caps (although you can easily simulate them through the use of a textbox). 

This will be improved in a future version of Aspose.Words.

See the following links in the documentation for further information:

- **ParagraphFormat.DropCapPositon**
- [ParagraphFormat.LinesToDrop](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.linestodrop.html)

|**Feature**|**Supported**|**Comment**|**See Also**|
| :- | :- | :- | :- |
|Drop Caps |Yes | | |
##### **Borders**

|**Feature**|**Supported**|**Comment**|**See Also**|
| :- | :- | :- | :- |
|Border Sides |Yes | |<p>- [ParagraphFormat.Borders](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.borders.html) </p><p>- [LineStyle](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.linestyle.html)</p>|
|Shadow |Yes | |- [Border.Shadow](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.border.shadow.html)|
|3D Frame |Yes | |- [Border.LineStyle](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.border.linestyle.html)|
|Style |Yes | |- **Border.LineStyle**|
|Color |Yes | |- [Border.Color](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.border.color.html)|
|Width |Yes | |- [Border.LineWidth](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.border.linewidth.html)|
|Distance from Text |Yes | |- [Border.DistanceFromText](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.border.distancefromtext.html)|
##### **Shading**
See the following link in the documentation for further information:

- [ParagraphFormat.Shading](http://www.aspose.com/documentation/.net-components/aspose.words-for-.net/aspose.words.paragraphformat.shading.html)

|**Feature**|**Supported**|**Comment**|**See Also**|
| :- | :- | :- | :- |
|Shading |Yes | | |
##### **Asian Typography**
Asian Typography settings is fully supported during conversion. However there is currently no API to access or modify these settings.

|**Feature**|**Supported**|**Comment**|**See Also**|
| :- | :- | :- | :- |
|Use Asian Rules for Controlling First and Last Characters |Yes | | |
|Allow Latin Text to Wrap in the Middle of a Word |Yes | | |
|Allow Hanging Punctuation |Yes | | |
|Allow Punctuation at Start of a Line to Compress |Yes | | |
|Automatically Adjust Space between Asian and Latin Text |Yes | | |
|Automatically Adjust Space between Asian Text and Numbers |Yes | | |
|Text Vertical Alignment |Yes | | |

