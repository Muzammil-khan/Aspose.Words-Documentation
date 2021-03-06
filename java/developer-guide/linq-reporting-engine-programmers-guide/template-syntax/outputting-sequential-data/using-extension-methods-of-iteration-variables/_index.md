---
title: Using Extension Methods of Iteration Variables
type: docs
weight: 30
url: /java/using-extension-methods-of-iteration-variables/
---

{{% alert color="primary" %}} 

LINQ Reporting Engine provides special extension methods for iteration variables of any type. You can normally use these extension methods in template expressions. The following list describes the extension methods.

- indexOf()

Returns the zero-based index of a sequence item that is represented by the corresponding iteration variable. You can use this extension method to distinguish sequence items with different indexes and then handle them in different ways. For example, given that items is an enumeration of the strings “item1”, “item2”, and “item3”, you can use the following template to enumerate them prefixing all of them but the first one with commas.

{{< highlight java >}}

 The items are: <<foreach [

    item in items]>><<[item.indexOf() != 0

        ? ", "

        : ""]>><<[item]>><</foreach>>.

{{< /highlight >}}

In this case, the engine produces a report as follows.

{{< highlight java >}}

 The items are: item1, item2, item3.

{{< /highlight >}}

- numberOf()

Returns the one-based index of a sequence item that is represented by the corresponding iteration variable. You can use this extension method to number sequence items without involving Microsoft Word® lists. For example, given the previous declaration of items, you can enumerate and number them in a document table using the following template.

|**No.** |**Item**|
| :- | :- |
|<p>{{< highlight java >}}</p><p> <<foreach [item</p><p>in items]>><<[</p><p>item.numberOf()]>></p><p>{{< /highlight >}}</p>|<p>{{< highlight java >}}</p><p> <<[item]>><</foreach>></p><p>{{< /highlight >}}</p>|
In this case, the engine produces a report as follows.

|**No.** |**Item**|
| :- | :- |
|1 |item1|
|2 |item2|
|3 |item3|
{{% /alert %}}
