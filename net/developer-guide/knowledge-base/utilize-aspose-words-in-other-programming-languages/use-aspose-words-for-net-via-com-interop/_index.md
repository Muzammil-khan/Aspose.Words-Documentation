---
title: Use Aspose.Words for .NET via COM Interop
type: docs
weight: 20
url: /net/use-aspose-words-for-net-via-com-interop/
---

{{% alert color="primary" %}} 

The information in this topic applies to scenarios where you want to use Aspose.Words for .NET via COM Interop in any of the following programming languages: 

- ASP
- Delphi
- JScript
- Perl
- PHP
- PowerBuilder
- Python
- VBScript
- Visual Basic

{{% /alert %}} 
### **Working with COM Interop**
Aspose.Words for .NET executes under the control of the .NET Framework and this is called managed code. Code written in all of the above languages runs outside the .NET Framework and it is called unmanaged code. Interaction between unmanaged code and Aspose.Words occurs via the .NET facility called COM Interop.

Aspose.Words objects are .NET objects, but when used via COM Interop, they appear as COM objects in your programming language. Therefore, it is best to make sure you know how to create and use COM objects in your programming language, before you start using Aspose.Words.

Here are the topics that you will eventually need to master: 

- Using COM objects in your programming language. See your programming language documentation and the language-specific topics further in this documentation.
- Working with COM objects exposed by .NET COM Interop. See [Interoperating With Unmanaged Code](http://msdn.microsoft.com/en-us/library/sd10k43k.aspx) and [Exposing .NET Framework Components to COM](http://msdn.microsoft.com/en-us/library/zsfww439%28v=vs.110%29.aspx) in MSDN.
- Aspose.Words document object model. See Aspose.Words [Programmer’s Guide](http://www.aspose.com/docs/display/wordsnet/Programmers+Guide) and [API Reference](http://www.aspose.com/docs/display/wordsnet/Aspose.Words+for+.NET+API+Reference).
#### **Register Aspose.Words for .NET with COM Interop**
After installation, you need to register Aspose.Words for COM Interop using the regasm.exe utility.

regasm.exe is a tool included in .NET Framework SDK. All the .NET Framework SDK tools are located in the *%windir%\Microsoft .NET\Framework\<FrameworkVersion>\ directory, for example *C:\Windows\Microsoft .NET\Framework\v2.0.50727* 

If you use Visual Studio, then the easiest way to launch regasm is to:

1. On the **Start** menu, select **Programs**, then **Microsoft Visual Studio 2010** and finally **Visual Studio Tools**.
1. Right-click **Visual Studio Command Prompt** and select **Run as Administrator**.
   This will launch the command prompt with all the necessary environment variables set.
1. Type: regasm <installdir>\bin\net2.0\Aspose.Words.dll /codebase
   where <installdir> is the directory where you installed Aspose.Words, typically **C:\Program Files (x86)\Aspose\Aspose.Words for .NET**. 
#### **ProgIDs**
ProgID stands for “programmatic identifier”, it is a name of a COM class that you need to use in order to create an object. 

Currently, Aspose.Words defines four publicly creatable COM objects. Their ProgIDs are: 

- [ComHelper](/pages/createpage.action?spaceKey=wordsnet&title=ComHelper+Class&linkCreation=true&fromPageId=2589106)
- [Document](/pages/createpage.action?spaceKey=wordsnet&title=Document+Class&linkCreation=true&fromPageId=2589106)
- [DocumentBuilder](/pages/createpage.action?spaceKey=wordsnet&title=DocumentBuilder+Class&linkCreation=true&fromPageId=2589106)
- [License](/pages/createpage.action?spaceKey=wordsnet&title=License+Class&linkCreation=true&fromPageId=2589106)

The ProgIDs consist of the library name ("Aspose.Words") and the class name. 
#### **Type Library**
During installation, the Aspose.Words.tlb (COM type library) is copied to your computer to:

- For .NET Framework 2.0, 3.0, 3.5 and 4.0 to **<installdir>\bin\net2.0**

If your programming language (for example Visual Basic or Delphi) allows you to reference a COM type library, then add a reference to **Aspose.Words.tlb** and you will be able to see all Aspose.Words classes, methods, properties and enumerations in your Object Browser. 
#### **Creating COM Objects**
The creation of a .NET object is similar to creation of a normal COM object:

**VBScript**

{{< highlight csharp >}}

 Dim helper

Set helper = CreateObject("Aspose.Words.ComHelper")



{{< /highlight >}}

Once created, you are able to access the object’s methods and properties, as if it was a COM object:

**VBScript**

{{< highlight csharp >}}

 Dim doc

Set doc = helper.Open("C:\my.doc")



{{< /highlight >}}

Some methods have overloads and they will be exposed by COM Interop with a numeric suffix added to them, except for the very first method that stays unchanged. For example, Document.Save method overloads become Document.Save, Document.Save_2, Document.Save_3, and so on. 

For more information, see the language-specific articles further in this documentation. 
#### **Creating a Wrapper Assembly**
If you need to use many of the Aspose.Words classes, methods and properties, consider creating a wrapper assembly (using C# or any other .NET programming language), that will help to avoid using Aspose.Words directly from unmanaged code.

A good approach is to develop a .NET assembly that references Aspose.Words and does all the work with it, and only exposes the minimal set of classes and methods to unmanaged code. Your application then should work just with your wrapper library. 

Reducing the number of classes and methods that you need to invoke via COM Interop could simplify your project, because using .NET classes via COM Interop often requires advanced skills. 
