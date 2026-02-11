---
title: 管理 Visio 宏启用 diagram 的 VBA 代码。
linktitle: Diagram VBA 项目
type: docs
weight: 200
url: /zh/net/working-with-vbaproject/
description: 使用 Aspose.Diagram 库添加 VBA 模块和修改 VBA 或宏。
---
## **添加 VBA 模块**
{{% alert color="primary" %}}

Aspose.Diagram 允许您使用 Aspose.Diagram 添加新的 VBA 模块和宏代码。请使用[**Diagram.VbaProject.Modules.Add()**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbamodulecollection/methods/add/index)在 diagram 中添加新的 VBA 模块的方法

{{% /alert %}}

下面的示例代码添加了一个新的 VBA 模块和宏代码，并以 VSDM 格式保存输出。一次，你将在Microsoft Visio中打开输出VSDM文件，点击**开发人员 > Visual Basic**菜单命令，您将看到一个名为“TestModule”的模块，在其中，您将看到以下宏代码。

{{< highlight "java" >}}

 Sub ShowMessage()

    MsgBox "Welcome to Aspose!"

End Sub

{{< /highlight >}}

下面是使用 VBA 模块和宏代码生成输出 VSDM 文件的示例代码。

```
{{< highlight "csharp" >}}
// ExStart:ApplyThemeToNewShape
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
//Add module
int index = diagram.VbaProject.Modules.Add(VbaModuleType.Procedural, "TestModule");
//Get module 
Aspose.Diagram.Vba.VbaModule module = diagram.VbaProject.Modules[index];
//Set module
module.Codes = "Attribute VB_Name = \"module2\"\r\n Sub Button1_Click()\r\n\r\n    MsgBox \"Welcome to Aspose!\"\r\n\r\nEnd Sub\r\n";

diagram.Save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

## **修改 VBA 或宏**

{{% alert color="primary" %}} 

您可以使用Aspose.Diagram修改VBA或宏代码。Aspose.Diagram添加了以下命名空间和类来读取和修改Visio文件中的VBA项目。

- Aspose.Diagram.Vba
- Vba项目
- Vba模块集合
- Vba模块

本文将向您展示如何使用 Aspose.Diagram 更改源文件 Visio 中的 VBA 或宏代码。

{{% /alert %}} 

以下示例代码加载源文件 Visio，其中包含以下 VBA 或宏代码

{{< highlight "java" >}}

 Sub Button1_Click()

    MsgBox "This is test message."

End Sub

{{< /highlight >}}

Aspose.Diagram示例代码执行后，VBA或Macro代码会修改成这样

{{< highlight "java" >}}

 Sub Button1_Click()

    MsgBox "This is Aspose.Diagram message."

End Sub

{{< /highlight >}}

您可以下载[源文件 Visio]()和[输出 Visio 文件]()从给定的链接。

```
{{< highlight "csharp" >}}
// ExStart:ApplyThemeToNewShape
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
//Get module 
Aspose.Diagram.Vba.VbaModule module = diagram.VbaProject.Modules[2];
//Set module
module.Codes = "Attribute VB_Name = \"module2\"\r\n Sub Button1_Click()\r\n\r\n    MsgBox \"This is Aspose.Diagram message.\"\r\n\r\nEnd Sub\r\n";

diagram.Save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

## **推进主题**
- [检查 VBA 代码是否已签名](/diagram/zh/net/check-if-vba-code-is-signed/)
