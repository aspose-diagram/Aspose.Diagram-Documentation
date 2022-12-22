---
title: 公共 API Aspose.Diagram 6.6.0 的变化
type: docs
weight: 30
url: /zh/java/public-api-changes-in-aspose-diagram-6-6-0/
---
{{% alert color="primary" %}} 

本文档描述了 Aspose.Diagram API 从版本 6.3.0 到 6.6.0 的更改，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.Diagram 中幕后行为的任何更改的描述。

{{% /alert %}} 
### **在 LoadFileFormat 类中添加 VSDM、VSSM 和 VSTM 格式**
此版本增加了对读取启用宏的 Visio 格式的支持。
### **在 SaveFileFormat 类中添加 VSDM、VSSM 和 VSTM 格式**
此版本增加了对编写启用宏的 Visio 格式的支持。
### **Visio Diagram 修改VBA模块代码**
我们添加了 Vba、VbaProject 和 VbaModule 类。这些类有助于控制 VBA 项目。使用这个新版本 6.6.0 或更高版本，开发人员可以提取和修改 VBA 模块代码。请检查此代码示例：

**Java**

{{< highlight "java" >}}

 // 加载现有的 Visio diagram

InputStream input = new FileInputStream("c:\\temp\\macro.vsdm");

Diagram diagram = 新的 Diagram（输入）；

// 提取VBA项目

VbaProject v = diagram.getVbaProject();

// 遍历模块并修改 VBA 宏代码

对于 (int i=0;i< diagram.getVbaProject().getModules().getCount();i++)

{

    VbaModule module =  diagram.getVbaProject().getModules().get(i);

    String code = module.getCodes();

    if (code.contains("This is test message."))

        code = code.replace("This is test message.", "This is Aspose.Diagram message.");

    module.setCodes (code);

}

// save the Visio diagram

diagram.Save("c:\\temp\\out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}
### **在 ForeignData 类中添加一个 getImageData 方法**
它将 ole 对象的图像表示为字节数组。除此之外，我们还增强了 OLE 对象的操作。开发人员现在也可以替换 Visio diagram 中的 OLE 对象。请查看此代码示例：

**Java**

{{< highlight "java" >}}

 String DirPath = "c:\\temp\\";

// load a Visio diagram

Diagram diagram = new Diagram(DirPath + "Drawing1.vsdx");

// get page of the Visio diagram by name

Page page = diagram.getPages().getPage("Page-1");

// get shape of the Visio diagram by ID

Shape OLE_Shape = page.getShapes().getShape(2);

// filter shapes by type Foreign

if (OLE_Shape.getType() == TypeValue.FOREIGN)

{

    if (OLE_Shape.getForeignData().getForeignType() == ForeignType.OBJECT)

    {

    	ByteArrayInputStream Ole_stream = new ByteArrayInputStream(OLE_Shape.getForeignData().getObjectData());

        // get format of the OLE file object

        com.aspose.words.FileFormatInfo info = com.aspose.words.FileFormatUtil.detectFileFormat(Ole_stream);

        if (info.getLoadFormat() == com.aspose.words.LoadFormat.DOC || info.getLoadFormat() == com.aspose.words.LoadFormat.DOCX)

        {

            // modify an OLE object

            com.aspose.words.Document doc = new com.aspose.words.Document(new ByteArrayInputStream(OLE_Shape.getForeignData().getObjectData()));

    	    doc.getRange().replace("testing", "Aspose", false, true);

            ByteArrayOutputStream outStream = new ByteArrayOutputStream();

            doc.save(outStream, com.aspose.words.SaveFormat.DOCX);

            // seve an OLE object

            OLE_Shape.getForeignData().setObjectData(outStream.toByteArray());

        }

    }

}

// save Visio diagram

diagram.save(DirPath + "modified.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
