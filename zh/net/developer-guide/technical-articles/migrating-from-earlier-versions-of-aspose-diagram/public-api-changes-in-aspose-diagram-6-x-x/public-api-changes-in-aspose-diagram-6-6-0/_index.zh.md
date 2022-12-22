---
title: 公共 API Aspose.Diagram 6.6.0 的变化
type: docs
weight: 20
url: /zh/net/public-api-changes-in-aspose-diagram-6-6-0/
---
{{% alert color="primary" %}} 

本文档描述了 Aspose.Diagram API 从版本 6.3.0 到 6.6.0 的更改，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.Diagram 中幕后行为的任何更改的描述。

{{% /alert %}} 
## **在 LoadFileFormat 类中添加 VSDM、VSSM 和 VSTM 格式**
此版本增加了对读取启用宏的 Visio 格式的支持。
## **在 SaveFileFormat 类中添加 VSDM、VSSM 和 VSTM 格式**
此版本增加了对编写启用宏的 Visio 格式的支持。
## **修改Visio Diagram中的VBA模块代码**
我们添加了 VbaModule、VbaModuleCollection、VbaProject、VbaProjectReference 和 VbaProjectReferenceCollection 类。这些类有助于控制 VBA 项目。使用这个新版本 6.6.0 或更高版本，开发人员可以提取和修改 VBA 模块代码。请检查此代码示例：

**C#**

{{< highlight "csharp" >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram(@"c:\temp\macro.vsdm", LoadFileFormat.VSDM);

// extract VBA project

Aspose.Diagram.Vba.VbaProject v = diagram.VbaProject;

// Iterate through the modules and modify VBA module code

foreach (VbaModule module in diagram.VbaProject.Modules)

{

    string code = module.Codes;

    if (code.Contains("This is test message."))

        code = code.Replace("This is test message.", "This is Aspose.Diagram message.");

    module.Codes = code;

}

// save the Visio diagram

diagram.Save(@"c:\temp\out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}

呈现宏“代码”时出错：为参数 lang 指定的值无效
## **在 ForeignData 类中添加一个 ImageData 属性**
它将 ole 对象的图像表示为字节数组。除此之外，我们还增强了 OLE 对象的操作。开发人员现在也可以替换 Visio diagram 中的 OLE 对象。请查看此代码示例：

**C#**

{{< highlight "csharp" >}}

 // load a Visio diagram

Diagram diagram = new Diagram(DirPath + "Drawing1.vsdx");

// get page of the Visio diagram by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// get shape of the Visio diagram by ID

Aspose.Diagram.Shape OLE_Shape = page.Shapes.GetShape(2);

// filter shapes by type Foreign

if (OLE_Shape.Type == Aspose.Diagram.TypeValue.Foreign)

{

    if (OLE_Shape.ForeignData.ForeignType == ForeignType.Object)

    {

        Stream Ole_stream = new MemoryStream(OLE_Shape.ForeignData.ObjectData);

        // get format of the OLE file object

        Aspose.Words.FileFormatInfo info = Aspose.Words.FileFormatUtil.DetectFileFormat(Ole_stream);

        if (info.LoadFormat == Aspose.Words.LoadFormat.Doc || info.LoadFormat == Aspose.Words.LoadFormat.Docx)

        {

            // modify an OLE object

            var doc = new Aspose.Words.Document(new MemoryStream(OLE_Shape.ForeignData.ObjectData));

            doc.Range.Replace("testing", "Aspose", false, true);

            MemoryStream outStream = new MemoryStream();

            doc.Save(outStream, Aspose.Words.SaveFormat.Docx);

            // save back an OLE object

            OLE_Shape.ForeignData.ObjectData = outStream.ToArray();

        }

    }

}

// save Visio diagram

diagram.Save(DirPath + "modified.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

呈现宏“代码”时出错：为参数 lang 指定的值无效
