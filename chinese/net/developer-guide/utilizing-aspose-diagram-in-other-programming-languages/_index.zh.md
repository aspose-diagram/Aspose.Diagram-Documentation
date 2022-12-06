---
title: 在其他编程语言中使用 Aspose.Diagram
type: docs
weight: 120
url: /zh/net/utilizing-aspose-diagram-in-other-programming-languages/
description: 本页介绍如何在其他编程语言中使用 Aspose.Diagram。
---
## **Use Aspose.Diagram for .NET via COM Interop**
本主题信息适用于开发者需要使用的场景[Aspose.Diagram for .NET](/diagram/zh/net/home/) via COM Interop in any supported language.
### **使用 COM 互操作**
Aspose.Diagram for .NET executes under the control of the .NET Framework and this is called managed code. The code written in all of the languages those runs outside the .NET Framework and it is called unmanaged code. Interaction between unmanaged code and Aspose.Diagram occurs via the .NET facility called COM Interop.

Aspose.Diagram objects are .NET objects, but when used via COM Interop, they appear as COM objects in your programming language. Therefore, it is best to make sure you know how to create and use COM objects in your programming language, before you start using [Aspose.Diagram for .NET](/diagram/zh/net/home/).

- 在 COM 世界中，我们区分 COM 服务器和 COM 客户端。 COM 服务器存储 COM 类，而 COM 客户端向 COM 服务器请求类实例，即 COM 对象。
-  COM 客户端或简单的客户端应用程序可以了解 COM 类的某些内容或完全不知道其方法和属性。因此，客户端应用程序可以在编译/构建时或仅在执行期间发现 COM 类结构。 “发现”的过程被称为绑定，因此我们有**早期绑定**和**后期绑定**.
- 简而言之，COM 类就像黑盒子，需要类型库才能使用它，这个二进制文件描述了 COM 类的方法、属性，任何支持使用 COM 对象的高级语言通常都有添加类型库的语法表达式，例如实例这是[**＃进口**](http://msdn.microsoft.com/en-us/library/8etzzkb6.aspx)在 C++。
- 类型库用于早期绑定。
-  COM 对象可以通过两种方式公开其方法和属性：通过**调度接口**（dispinterface）并在其**虚表**（虚函数表）。
- 在**调度接口**，每个方法和属性都由一个唯一的成员标识；该成员是函数的调度标识符（或**显示ID**).
- **虚表**只是一组指向 COM 类接口支持的函数的指针。
- 通过两个接口公开其方法的对象支持**双界面**.
- 两种类型的绑定都有优点。早期绑定为您提供了更高的性能和编译时语法检查。当您编写您打算成为的客户时，后期绑定是最有利的***与未来版本兼容***你的 COM 类。通过后期绑定，来自类型库的信息不会“硬连接”到您的客户端，因此您可以更加确信您的客户端可以使用未来版本的 COM 类而无需更改代码。
- 延迟绑定机制有一个很大的优势：如果 COM DLL 的创建者决定发布一个新版本，具有不同的功能界面布局，任何调用这些方法的代码都不会崩溃，除非这些方法不再可用；即使**虚表**不同之处在于后期绑定设法发现新的 DISPID 并调用适当的方法。

以下是您最终需要掌握的主题：

- 在您的编程语言中使用 COM 对象。请参阅本文档中的编程语言文档和特定于语言的主题。
- 使用 .NET COM Interop 公开的 COM 对象。看[与非托管代码互操作](https://docs.microsoft.com/en-us/dotnet/framework/interop/)和[将 .NET Framework 组件暴露给 COM](https://docs.microsoft.com/en-us/dotnet/framework/interop/exposing-dotnet-components-to-com)在 MSDN 中。
-  Aspose.Diagram 文档对象模型。看[Aspose.Diagram 程序员指南](https://docs.aspose.com/diagram/net/developer-guide/)和[API 参考](https://reference.aspose.com/diagram/net).
#### **使用 COM Interop 注册 Aspose.Diagram for .NET**
您需要安装 Aspose.Diagram for .NET 并确保它已注册到 COM Interop（确保它可以从非托管代码调用）。

手动为 COM Interop 注册 Aspose.Diagram for .NET：

1. 来自**开始**菜单，选择**所有程序**， 然后**Microsoft Visual Studio**, **Visual Studio Tools**最后，**Visual Studio Command Prompt**.在某些操作系统中，它也位于以下位置：“C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\bin\x64”
1. 输入命令注册程序集：
   1. .NET Framework 2.0
regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net2.0\Aspose.Diagram.dll" /codebase
   1. .NET Framework 3.5
 regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net3.5\Aspose.Diagram.dll" /codebase
   1. .NET Framework 4.0
 regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net4.0\Aspose.Diagram.dll" /codebase

{{% alert color="primary" %}} 

请注意，仅当 Aspose.Diagram.dll 不在 GAC 中时 /codebase 才是必需的，使用此选项会使 regasm 将程序集路径放入注册表中。

{{% /alert %}} {{% alert color="primary" %}} 

 regasm.exe 是 .NET Framework SDK 中包含的一个工具。所有.NET Framework SDK工具都位于*\Microsoft .NET\Framevork\<框架版本>*目录，例如*C:\Windows\Microsoft .NET\Framework\v4.0.30319*. If you use Visual Studio .NET:
来自**开始**菜单，选择**程式**， 其次是**Microsoft Visual Studio .NET**， 然后**Visual Studio .NET Tools**最后，**Visual Studio .NET 2003 Command Prompt**.
它运行命令提示符，并设置了所有必要的环境变量。

{{% /alert %}} 
##### **ProgIDs**
ProgID 代表“编程标识符”。它是用于创建对象的 COM 类的名称。 ProgID 由库名“Aspose.Diagram”和类名组成。
##### **类型库**
如果您的编程语言（例如 Visual Basic 或 Delphi）允许您引用 COM 类型库，则添加对 Aspose.Diagram.tlb 的引用并在您的对象浏览器中查看所有 Aspose.Diagram for .NET 类、方法、属性和枚举。

要生成 TLB 文件：

- .NET Framework 2.0
 regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net2.0\Aspose.Diagram.dll" /tlb: "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net2.0\0761734" /codebasetlb
- .NET Framework 3.5
 regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net3.5\Aspose.Diagram.dll" /tlb: "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net3.5\0761734" /codebasetlb
- .NET Framework 4.0
regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net4.0\Aspose.Diagram.dll" /tlb: "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net4.0\0761734" /codebasetlb
#### **创建 COM 对象**
COM 对象的创建类似于普通 .NET 对象的创建。一旦创建，您就可以访问该对象的方法和属性，就好像它是一个 COM 对象一样。

有些方法有重载，它们将由 COM Interop 公开，并添加一个数字后缀，但第一个方法保持不变。例如，Diagram.Save 方法重载变为 Diagram.Save、Diagram.Save_2 等。

{{% alert color="primary" %}} 

有关详细信息，请参阅本文档中特定语言的文章。

{{% /alert %}} 
## **Aspose.Diagram 资源**
以下是您完成任务可能需要的一些有用资源的链接。
- [Aspose.Diagram for Java 在线文档](https://docs.aspose.com/diagram/java/)
- [Aspose.Diagram for Node.js via Java Online Documentation](https://docs.aspose.com/diagram/nodejsjava/)
- [Aspose.Diagram for Python via Java Online Documentation](https://docs.aspose.com/diagram/pythonjava/)

##### **创建包装程序集**
如果您需要使用许多 Aspose.Diagram for .NET 类、方法和属性，请考虑创建一个包装程序集（使用 C# 或任何其他 .NET 编程语言）。包装器程序集有助于避免直接从非托管代码使用 Aspose.Diagram for .NET。

一个好的方法是开发一个 .NET 程序集，该程序集引用 Aspose.Diagram for .NET 并使用它完成所有工作，并且只向非托管代码公开一组最小的类和方法。然后您的应用程序应该只与您的包装器库一起工作。

Reducing the number of classes and methods that you need to invoke via COM Interop simplifies the project. Using .NET classes via COM Interop often requires advanced skills. 
## **使用 COM Interop 在 PHP 中创建一个空的 Visio 绘图**
### **先决条件**
配置您的 PHP 以使用 COM。看<http://www.php.net/manual/en/ref.com.php>.有关更多信息，请查看名为[Use Aspose.Diagram for .NET via COM Interop](/diagram/zh/net/home/).
### **创建一个空的 Visio 绘图**
这是一个简单的应用程序，向您展示如何使用以下方法创建空的 Visio 绘图[Aspose.Diagram for .NET](/diagram/zh/net/home/) in PHP via COM Interop.

**PHP**

{{< highlight "csharp" >}}

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
