---
title: Utilize Aspose.Diagram in Other Programming Languages
type: docs
weight: 120
url: /net/utilize-aspose-diagram-in-other-programming-languages/
---

## **Use Aspose.Diagram for .NET via COM Interop**
The information in this topic applies to scenarios where developers require to use [Aspose.Diagram for .NET](/diagram/net/home/) via COM Interop in any supported language.
### **Working with COM Interop**
Aspose.Diagram for .NET executes under the control of the .NET Framework and this is called managed code. The code written in all of the languages those runs outside the .NET Framework and it is called unmanaged code. Interaction between unmanaged code and Aspose.Diagram occurs via the .NET facility called COM Interop.

Aspose.Diagram objects are .NET objects, but when used via COM Interop, they appear as COM objects in your programming language. Therefore, it is best to make sure you know how to create and use COM objects in your programming language, before you start using [Aspose.Diagram for .NET](/diagram/net/home/).

- In COM world we distinguish COM server and COM client. COM server stored COM classes while COM client asks COM server for classes instances, i.e. COM objects.
- COM client or simply client application can know about COM class contents something or be totally unaware about its methods and properties. Therefore client application can discover COM class structure on compiling/building or only during execution. Process of "discovery" is known as binding and so we have **early binding** and **late binding**.
- in brief COM class is like black box and to work with it type library is needed, this binary file has description of COM class methods, properties and any high level language which supports working with COM objects often has syntax expression for adding type library, for instance this is [**#import**](http://msdn.microsoft.com/en-us/library/8etzzkb6.aspx) in C++.
- type library is used for early binding.
- a COM object can expose its methods and properties in two ways: by means of a **dispatch interface** (dispinterface) and in its **vtable** (virtual function table).
- within the **dispinterface**, each method and property is identified by a unique member; this member is the function's dispatch identifier(or **DispID**).
- **vtable** is just a set of pointers to functions that the COM class interface supports.
- an object that exposes its methods through both interfaces supports a **dual interface**.
- there are advantages to both types of binding. Early binding provides you with increased performance and compile-time syntax checking. Late binding is most advantageous when you are writing clients that you intend to be ***compatible with future versions*** of your COM class. With late binding, information from the type library is not "hard-wired" into your client, so you can have greater confidence that your client can work with future versions of COM class without code changes.
- late binding mechanism has a big advantage: if the creator of the COM DLL decides to release a new version, with a different function interface layout, any code calling those methods won't crash unless the methods are no longer available; even if the **vtable** is different late binding manages to discover the new DISPIDs and call appropriate methods.

Here are the topics that you will eventually need to master: 

- Using COM objects in your programming language. See your programming language documentation and the language-specific topics further in this documentation.
- Working with COM objects exposed by .NET COM Interop. See [Interoperating With Unmanaged Code](http://msdn.microsoft.com/en-us/library/sd10k43k.aspx) and [Exposing .NET Framework Components to COM](http://msdn.microsoft.com/en-us/library/zsfww439%28v=vs.110%29.aspx) in MSDN.
- Aspose.Diagram document object model. See [Aspose.Diagram Programmer’s Guide](http://www.aspose.com/docs/pages/viewpage.action?pageId=10846801) and [API Reference](http://www.aspose.com/docs/display/diagramnet/Aspose.Diagram+for+.NET+API+Reference).
#### **Register Aspose.Diagram for .NET with COM Interop**
You need to install Aspose.Diagram for .NET and make sure it is registered with COM Interop (ensuring that it can be called from unmanaged code).

To register Aspose.Diagram for .NET for COM Interop manually:

1. From the **Start** menu, select **All Programs**, then **Microsoft Visual Studio**, **Visual Studio Tools** and, finally, **Visual Studio Command Prompt**. In some operating systems, it is also available at the location: "C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\bin\x64"
1. Enter the command to register the assembly: 
   1. .NET Framework 2.0
      regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net2.0\Aspose.Diagram.dll" /codebase
   1. .NET Framework 3.5
      regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net3.5\Aspose.Diagram.dll" /codebase
   1. .NET Framework 4.0
      regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net4.0\Aspose.Diagram.dll" /codebase

{{% alert color="primary" %}} 

Pay attention that /codebase is necessary only if Aspose.Diagram.dll is not in GAC, using this option makes regasm put path for assembly in registry.

{{% /alert %}} {{% alert color="primary" %}} 

regasm.exe is a tool included in .NET Framework SDK. All the .NET Framework SDK tools are located in the *\Microsoft .NET\Framevork\<FrameworkVersion>* directory, for example *C:\Windows\Microsoft .NET\Framework\v4.0.30319*. If you use Visual Studio .NET:
From the **Start** menu, select **Programs**, followed by **Microsoft Visual Studio .NET**, then **Visual Studio .NET Tools** and, finally, **Visual Studio .NET 2003 Command Prompt**.
It runs a command prompt with all the necessary environment variables set. 

{{% /alert %}} 
##### **ProgIDs**
ProgID stands for “programmatic identifier”. It is the name of a COM class that used to create an object. ProgIDs consist of the library name "Aspose.Diagram" and the class name.
##### **Type Library**
If your programming language (for example Visual Basic or Delphi) allows you to reference a COM type library, then add a reference to Aspose.Diagram.tlb and to see all Aspose.Diagram for .NET classes, methods, properties and enumerations in your Object Browser.

To generate a TLB file:

- .NET Framework 2.0
  regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net2.0\Aspose.Diagram.dll" /tlb: "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net2.0\Aspose.Diagram.tlb" /codebase
- .NET Framework 3.5
  regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net3.5\Aspose.Diagram.dll" /tlb: "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net3.5\Aspose.Diagram.tlb" /codebase
- .NET Framework 4.0
  regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net4.0\Aspose.Diagram.dll" /tlb: "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net4.0\Aspose.Diagram.tlb" /codebase
#### **Creating COM Objects**
The creation of a COM object is similar to creation of a normal .NET object. Once created, you are able to access the object’s methods and properties, as if it was a COM object.

Some methods have overloads and they will be exposed by COM Interop with a numeric suffix added to them, except for the very first method that stays unchanged. For example, the Diagram.Save method overloads become Diagram.Save, Diagram.Save_2, and so on.

{{% alert color="primary" %}} 

For more information, see the language-specific articles further in this documentation. 

{{% /alert %}} 
##### **Creating a Wrapper Assembly**
If you need to use many of Aspose.Diagram for .NET classes, methods and properties, consider creating a wrapper assembly (using C# or any other .NET programming language). Wrapper assemblies help help to avoid using Aspose.Diagram for .NET directly from unmanaged code.

A good approach is to develop a .NET assembly that references Aspose.Diagram for .NET and does all the work with it, and only exposes a minimal set of classes and methods to unmanaged code. Your application then should work just with your wrapper library.

Reducing the number of classes and methods that you need to invoke via COM Interop simplifies the project. Using .NET classes via COM Interop often requires advanced skills. 
## **Create an Empty Visio Drawing in PHP using COM Interop**
### **Prerequisites**
Configure your PHP to work with COM. See <http://www.php.net/manual/en/ref.com.php>. For more information, please check the article named [Use Aspose.Diagram for .NET via COM Interop](/pages/createpage.action?spaceKey=diagramnet&title=Use+Aspose.Diagram+for+.NET+via+COM+Interop&linkCreation=true&fromPageId=18350127).
### **Creating an Empty Visio Drawing**
This is a simple application that shows you how to create an empty Visio drawing using [Aspose.Diagram for .NET](/diagram/net/home/) in PHP via COM Interop.

**PHP**

{{< highlight csharp >}}

 <?php

echo "<h3>Calling Aspose.Diagram for .NET from PHP using COM Interoperatibility</h3>";

//set license

$lic = new COM("Aspose.Diagram.License");

$lic->SetLicense("D:\ASPOSE\Licences\Aspose.Total licenses\Aspose.Total.lic");

// create a new instance of Diagram object using COM interop

$diagram = new COM("Aspose.Diagram.Diagram");

// Save the Visio drawing in the VDX format

$diagram->Save("d:\diagramtest\MyOutput.vdx", 0);

?>



{{< /highlight >}}
