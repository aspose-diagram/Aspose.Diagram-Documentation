---
title: 设置打印选项
type: docs
weight: 10
url: /zh/net/setting-print-options/
description: 本节介绍如何使用 Aspose.Diagram 设置打印选项。
---
{{% alert color="primary" %}}

有时，需要为页面配置页面设置以控制打印。这些页面设置设置提供了各种选项。

{{% /alert %}}

## **设置打印选项**

Aspose.Diagram 完全支持页面设置选项。本文介绍了如何使用 Aspose.Diagram 设置页面选项，并显示了用于设置的代码示例：

 Aspose.Diagram提供了一个类，[**页**](https://reference.aspose.com/diagram/net/aspose.diagram/page) ，代表一个 Microsoft Visio 文件。这[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page)类包含一个[**页数**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection)允许访问 Visio 文件中每个页面的集合。一个页面由[**页**](https://reference.aspose.com/diagram/net/aspose.diagram/page)班级。

这[**页表**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet)类提供了[**打印道具**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)用于设置页面的页面设置选项的属性。事实上，这[**打印道具**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)属性是[**页表**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet)用于为打印页面设置不同页面布局选项的类。这[**打印道具**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)类提供用于设置页面设置选项的各种属性。下面讨论其中一些特性。

### **打印页面方向**

打印页面方向可以设置为纵向或横向使用[**打印道具**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)班级'[**打印页面方向**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/printpageorientation)财产。这[**打印页面方向**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/printpageorientation)属性接受中的预定义值之一[**打印页面方向值**](https://reference.aspose.com/diagram/net/aspose.diagram/printpageorientationvalue)枚举，如下所示。

|**打印页面方向类型**|**描述**|
|:- |:- |
|与打印机相同|与打印机方向相同|
|景观|横向|
|肖像|纵向|

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Get page
Aspose.Diagram.Page page = diagram.Pages.GetPage(0);

//Set PrintPageOrientation
page.PageSheet.PrintProps.PrintPageOrientation.Value = PrintPageOrientationValue.Landscape;

{{< /highlight >}}
```

### **比例因子**

可以通过调整比例因子来缩小或放大页面的大小[**秤X**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/scalex)财产。

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Set ScaleX and ScaleY
diagram.Pages[0].PageSheet.PrintProps.ScaleX.Value = 1;
diagram.Pages[0].PageSheet.PrintProps.ScaleY.Value = 1;

{{< /highlight >}}
```
