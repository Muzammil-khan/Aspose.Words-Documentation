---
title: Introduction to LINQ Reporting Engine
type: docs
weight: 10
url: /net/introduction-to-linq-reporting-engine/
---

## **Introduction**
LINQ Reporting Engine is a part of the [Aspose.Words API](https://products.aspose.com/words/net) that enables you to build reports using an extended set of reporting features. The engine enables you to reference business objects of your application in report templates directly, which agrees well with [Domain-Driven Design](http://en.wikipedia.org/wiki/Domain-driven_design) widely used in modern software development. Moreover, the engine uses a subset of C# language in its template syntax. These features enable you as a developer to compose report templates in a familiar and intuitive way.
## **Origin of LINQ Reporting Engine**
Historically, [Aspose.Words Mail Merge](http://www.aspose.com/docs/display/wordsnet/About+Mail+Merge+in+Aspose.Words) was the first attempt to bring reporting features to the Aspose.Words API. However, the main purpose of Aspose.Words Mail Merge is mimicking Microsoft Word® Mail Merge. That is why the mail-merge-template syntax is based on Microsoft Word® merge fields. This fact makes it impossible to extend the template syntax keeping it concise, clear, and simple for users.

The concept of LINQ Reporting Engine resolves this issue by using various single-purpose text tags, rather than reusing the same merge fields for various purposes. In general, this approach makes the template syntax much shorter and clearer. Thus, for example, the adding of a new tag type does not pollute the syntax that much. This fact makes the syntax much more extensible and able to satisfy growing customers’ needs.
## **LINQ Reporting Engine Features**
LINQ Reporting Engine enables you to build reports in a similar way as Aspose.Words Mail Merge does. The engine provides the API that enables you to populate template documents with data that comes from various sources.

In contrast to Aspose.Words Mail Merge, LINQ Reporting Engine works with templates based on tags that you can form using just plain text. These tags define expressions and their roles during a report building process. Then, while building a report, the following procedure takes place:

1. The expressions are sequentially evaluated against a passed data source object.
1. The results of the expressions are processed by the engine according to their roles.
1. The corresponding tags are replaced with appropriate contents.

While composing expressions, you can use a subset of C# language that satisfies [C# Language Specification 5.0](http://www.microsoft.com/en-us/download/details.aspx?id=7029). Common reporting data manipulations such as grouping, sorting, and others are included in the expression syntax in the form of [IEnumerable<T>](http://msdn.microsoft.com/en-us/library/9eekhta0\(v=vs.110\).aspx) extension methods. LINQ Reporting Engine gained its name because of this feature.

You can use common Aspose.Words Mail Merge data source objects such as [DataSet](http://msdn.microsoft.com/en-us/library/system.data.dataset\(v=vs.110\).aspx), [DataTable](http://msdn.microsoft.com/en-us/library/system.data.datatable\(v=vs.110\).aspx), and others while working with LINQ Reporting Engine as well. The engine provides a simplified expression syntax to work with such objects. For example, a data table is treated as a collection of its rows. That is, you can normally apply IEnumerable<T> extension methods to it. A single data row, in turn, is treated as if it was an object that has the same set of fields that the row has.

In addition to traditional data sources, the engine enables you to use custom ones. Custom data source objects are not treated in a special way by the engine. That is while working with such objects, you can use the same expression syntax as you use while writing C# code. Moreover, you can use accessible members of any custom type that can implement any complex logic. This feature makes the engine very flexible and suitable almost for any specific need while building a report.
## **Hello World Example**
A "Hello, World" example is traditionally used to introduce features of a programming language or software with a simple use case. Here is the example for LINQ Reporting Engine. Assume that you have the Sender class defined in your application as follows:

{{< gist "aspose-words" "9a306a41bb6aea8adfcabf5a575c5718" "Examples-CSharp-LINQ-Sender-Sender.cs" >}}

To produce a report containing a message of a concrete sender on its behalf, you can use a template document with the following content.

{{< highlight java >}}

 <<[s.Name]>> says: "<<[s.Message]>>."

{{< /highlight >}}

To build a report from the template, you can use the following source code. You can download the template file of this example from [here](https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/LINQ/HelloWorld.doc).

{{< gist "aspose-words" "9a306a41bb6aea8adfcabf5a575c5718" "Examples-CSharp-LINQ-HelloWorld-HelloWorld.cs" >}}

After the source code is executed, the template document is populated with the data about the sender, and the document becomes a ready report with the following content.

{{< highlight java >}}

 LINQ Reporting Engine says: "Hello, World."

{{< /highlight >}}

After the report document is built, you can save it or perform any other tasks on it using [Aspose.Words API](https://apireference.aspose.com/net/words) in your code.
## **Enumeration Extension Methods**
LINQ Reporting Engine enables you to perform common manipulations on a sequential data through the engine's built-in extension methods for IEnumerable. These extension methods mimic some extension methods of [IEnumerable<T>](http://msdn.microsoft.com/en-us/library/9eekhta0\(v=vs.110\).aspx) providing the same signatures and behavior features. Thus, you can group, sort, and perform other sequential data manipulations in template expressions in a familiar way.

The following table describes these built-in extension methods. The following notation conventions are used within the table:

- Selector stands for a lambda function returning a value and taking an enumeration item as its single argument. See “Using Lambda Functions” for more information.
- ComparableSelector stands for Selector returning [IComparable](http://msdn.microsoft.com/en-US/library/system.icomparable\(v=vs.110\).aspx).
- Predicate stands for Selector returning a Boolean value.

Examples in the following table are given using persons and otherPersons, enumerations of instances of the Person class that is defined as follows.

{{< highlight java >}}

 public class Person

{

    public String Name { get { ... } }

    public int Age { get { ... } }

    public IEnumerable<Person> Children { get { ... } }

    ...

}

{{< /highlight >}}

|**Extension Method**|**Examples and Notes**|
| :- | :- |
|All(Predicate)|<p>{{< highlight java >}}</p><p> persons.All(p => p.Age < 50)</p><p>{{< /highlight >}}</p>|
|Any()|<p>{{< highlight java >}}</p><p> persons.Any()</p><p>{{< /highlight >}}</p>|
|Any(Predicate)|<p>{{< highlight java >}}</p><p> persons.Any(p => p.Name == "John Smith")</p><p>{{< /highlight >}}</p>|
|Average(Selector)|<p>{{< highlight java >}}</p><p> persons.Average(p => p.Age)</p><p>{{< /highlight >}}</p><p>The input selector must return a value of any type that has predefined or user-defined addition and division operators.</p>|
|Concat(IEnumerable)|<p>{{< highlight java >}}</p><p> persons.Concat(otherPersons)</p><p>{{< /highlight >}}</p><p>An implicit reference conversion must exist between types of items of concatenated enumerations.</p>|
|Contains(Object)|<p>{{< highlight java >}}</p><p> persons.Contains(otherPersons.First())</p><p>{{< /highlight >}}</p>|
|Count()|<p>{{< highlight java >}}</p><p> persons.Count()</p><p>{{< /highlight >}}</p>|
|Count(Predicate)|<p>{{< highlight java >}}</p><p> persons.Count(p => p.Age > 30)</p><p>{{< /highlight >}}</p>|
|Distinct()|<p>{{< highlight java >}}</p><p> persons.Distinct()</p><p>{{< /highlight >}}</p>|
|First()|<p>{{< highlight java >}}</p><p> persons.First()</p><p>{{< /highlight >}}</p>|
|First(Predicate)|<p>{{< highlight java >}}</p><p> persons.First(p => p.Age > 30)</p><p>{{< /highlight >}}</p>|
|FirstOrDefault()|<p>{{< highlight java >}}</p><p> persons.FirstOrDefault()</p><p>{{< /highlight >}}</p>|
|FirstOrDefault(Predicate)|<p>{{< highlight java >}}</p><p> persons.FirstOrDefault(p => p.Age > 30)</p><p>{{< /highlight >}}</p>|
|GroupBy(Selector)|<p>{{< highlight java >}}</p><p> persons.GroupBy(p => p.Age)</p><p>{{< /highlight >}}</p><p>Or</p><p>{{< highlight java >}}</p><p> persons.GroupBy(</p><p>    p => new</p><p>    {</p><p>        Age = p.Age,</p><p>        Count = p.Children.Count()</p><p>    })</p><p>{{< /highlight >}}</p><p>This method returns an enumeration of group objects. Each group has a unique key defined by the input selector and contains items of the source enumeration associated with this key. You can access the key of a group instance using the Key property. You can treat a group itself as an enumeration of items that the group contains.</p>|
|Last()|<p>{{< highlight java >}}</p><p> persons.Last()</p><p>{{< /highlight >}}</p>|
|Last(Predicate)|<p>{{< highlight java >}}</p><p> persons.Last(p => p.Age > 100)</p><p>{{< /highlight >}}</p>|
|LastOrDefault()|<p>{{< highlight java >}}</p><p> persons.LastOrDefault()</p><p>{{< /highlight >}}</p>|
|LastOrDefault(Predicate)|<p>{{< highlight java >}}</p><p> persons.LastOrDefault(p => p.Age > 100)</p><p>{{< /highlight >}}</p>|
|Max(ComparableSelector)|<p>{{< highlight java >}}</p><p> persons.Max(p => p.Age)</p><p>{{< /highlight >}}</p>|
|Min(ComparableSelector)|<p>{{< highlight java >}}</p><p> persons.Min(p => p.Age)</p><p>{{< /highlight >}}</p>|
|OrderBy(ComparableSelector)|<p>{{< highlight java >}}</p><p> persons.OrderBy(p => p.Age)</p><p>{{< /highlight >}}</p><p>Or</p><p>{{< highlight java >}}</p><p> persons.OrderBy(p => p.Age)</p><p>    .ThenByDescending(p => p.Name)</p><p>{{< /highlight >}}</p><p>Or</p><p>{{< highlight java >}}</p><p> persons.OrderBy(p => p.Age)</p><p>    .ThenByDescending(p => p.Name)</p><p>    .ThenBy(p => p.Children.Count())</p><p>{{< /highlight >}}</p><p>This method returns an enumeration ordered by a single key. To specify additional ordering keys, you can use the following extension methods of an ordered enumeration:</p><p>- ThenBy(ComparableSelector)</p><p>- ThenByDescending(ComparableSelector)</p>|
|OrderByDescending(ComparableSelector)|<p>{{< highlight java >}}</p><p> persons.OrderByDescending(p => p.Age)</p><p>{{< /highlight >}}</p><p>Or</p><p>{{< highlight java >}}</p><p> persons.OrderByDescending(p => p.Age)</p><p>    .ThenByDescending(p => p.Name)</p><p>{{< /highlight >}}</p><p>Or</p><p>{{< highlight java >}}</p><p> persons.OrderByDescending(p => p.Age)</p><p>    .ThenByDescending(p => p.Name)</p><p>    .ThenBy(p => p.Children.Count())</p><p>{{< /highlight >}}</p><p>See the previous note.</p>|
|Single()|<p>{{< highlight java >}}</p><p> persons.Single()</p><p>{{< /highlight >}}</p>|
|Single(Predicate)|<p>{{< highlight java >}}</p><p> persons.Single(</p><p>    p => p.Name == "John Smith")</p><p>{{< /highlight >}}</p>|
|SingleOrDefault()|<p>{{< highlight java >}}</p><p> persons.SingleOrDefault()</p><p>{{< /highlight >}}</p>|
|SingleOrDefault(Predicate)|<p>{{< highlight java >}}</p><p> persons.SingleOrDefault(</p><p>    p => p.Name == "John Smith")</p><p>{{< /highlight >}}</p>|
|Skip(int)|<p>{{< highlight java >}}</p><p> persons.Skip(10)</p><p>{{< /highlight >}}</p>|
|SkipWhile(Predicate)|<p>{{< highlight java >}}</p><p> persons.SkipWhile(p => p.Age < 21)</p><p>{{< /highlight >}}</p>|
|Sum(Selector)|<p>{{< highlight java >}}</p><p> persons.Sum(p => p.Children.Count())</p><p>{{< /highlight >}}</p><p>The input selector must return a value of any type that has a predefined or user-defined addition operator.</p>|
|Take(int)|<p>{{< highlight java >}}</p><p> persons.Take(5)</p><p>{{< /highlight >}}</p>|
|TakeWhile(Predicate)|<p>{{< highlight java >}}</p><p> persons.TakeWhile(p => p.Age < 50)</p><p>{{< /highlight >}}</p>|
|Union(IEnumerable)|<p>{{< highlight java >}}</p><p> persons.Union(otherPersons)</p><p>{{< /highlight >}}</p><p>An implicit reference conversion must exist between types of items of united enumerations.</p>|
|Where(Predicate)|<p>{{< highlight java >}}</p><p> persons.Where(p => p.Age > 18)</p><p>{{< /highlight >}}</p>|
## **Technical FAQ**
This section reveals some technical aspects and implementation details related to LINQ Reporting Engine. This information can be useful for you while making design decisions for your applications. The information is provided in a question-answer form.
### **How is the type of an enumeration item implicitly determined by the engine in template expressions?**
If you do not specify the type of an enumeration item in a foreach statement or lambda function signature within your template explicitly, the type is implicitly determined by the engine from the type of the enumeration as follows:

1. If the enumeration represents a DataTable instance, then the item type is DataRow.
1. Otherwise, if the enumeration represents a DataView instance, then the item type is DataRowView.
1. Otherwise, if the enumeration implements IDataReader, then the item type is IDataRecord.
1. Otherwise, if the enumeration represents child rows of a DataRow instance, then the item type is DataRow.
1. Otherwise, if the enumeration implements generic IEnumerable<T>, then the item type is a type argument corresponding to T. Note, that the engine does not support enumerations that implement IEnumerable<T> multiple times using different type arguments.
1. Otherwise, the item type is Object.
### **Does the engine cooperate with LINQ providers?**
The engine does not cooperate with [LINQ providers](http://msdn.microsoft.com/en-us/library/vstudio/bb882640\(v=vs.110\).aspx). To be aware of the consequences of this feature, consider the following example. Assume, that you have the City and Person classes defined in your application as follows.

{{< highlight java >}}

 public class City

{

    public IList<Person> Persons { get { ... } }

    ...

}

public class Person

{

    public String Name { get { ... } }

    public int Age { get { ... } }

    ...

    }

}

{{< /highlight >}}

Given that city is an instance of the City class, consider the evaluation of the following template expression by the engine.

{{< highlight java >}}

 city.Persons.Where(p => p.Age > 30).OrderBy(p => p.Name)

{{< /highlight >}}

If you use an ORM to provide an interaction of your application with an SQL database in conjunction with a LINQ provider for the ORM, then you most likely expect an SQL query like the following one to be performed in the background while evaluating the template expression.

{{< highlight java >}}

 SELECT *

    FROM Persons

    WHERE CityId = @CityId AND Age > 30

    ORDER BY Name

{{< /highlight >}}

However, since the engine does not cooperate with LINQ providers, the actual SQL query, in this case, is as follows.

{{< highlight java >}}

 SELECT *

    FROM Persons

    WHERE CityId = @CityId

{{< /highlight >}}

That is, the engine makes an eager call before applying its built-in extension methods. In some cases, this feature can lead to significant performance overhead. So, if the performance of your application is your primary concern, then consider a preparing of your sequential data outside your templates. That is, pass to the engine a sequential data that is already filtered, ordered, grouped, and so forth.
### **Have I do something special to merge the Aspose.Words assembly with another assembly?**
You can normally use a tool like [ILMerge](http://research.microsoft.com/en-us/people/mbarnett/ilmerge.aspx) to merge the Aspose.Words assembly with another assembly. However, if you use the functionality of LINQ Reporting Engine, add the following attribute to the target assembly.

{{< highlight java >}}

 [assembly: InternalsVisibleTo(

    "TargetAssemblyName" +

    ".ReportingDynamics" +

    ", PublicKey=TargetAssemblyPublicKey")]

{{< /highlight >}}

TargetAssemblyName and TargetAssemblyPublicKey stand for the name of your target assembly and its public key (not a public key token) respectively.

Despite the InternalsVisibleTo attribute applied, you can normally use obfuscation routines on your target assembly, if needed. Obfuscation does not harm a functionality of LINQ Reporting Engine.
