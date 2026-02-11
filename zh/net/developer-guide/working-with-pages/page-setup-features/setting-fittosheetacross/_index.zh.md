---
title: 设置 FitToSheetAcross
type: docs
weight: 10
url: /zh/net/setting-fittosheetacross/
description: 本节介绍如何使用 Aspose.Diagram 设置 fittosheetacross。
---
{{% alert color="primary" %}}

有时，需要为页面配置页面设置以控制打印。这些页面设置设置提供了各种选项。

{{% /alert %}}

## **设置 FitToSheetAcross**

Aspose.Diagram 完全支持页面设置选项。本文介绍了如何使用 Aspose.Diagram 设置页面选项，并显示了用于设置的代码示例：

 Aspose.Diagram提供了一个类，[**页**](https://reference.aspose.com/diagram/net/aspose.diagram/page) ，代表一个 Microsoft Visio 文件。这[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page)类包含一个[**页数**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection)允许访问 Visio 文件中每个页面的集合。一个页面由[**页**](https://reference.aspose.com/diagram/net/aspose.diagram/page)班级。

这[**页表**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet)类提供了[**打印道具**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)用于设置页面的页面设置选项的属性。事实上，这[**打印道具**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)属性是[**页表**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet)用于为打印页面设置不同页面布局选项的类。这[**打印道具**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)类提供用于设置页面设置选项的各种属性。下面讨论其中一些特性。

### **FitToSheetAcross**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Print();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

PrintProps printProps = diagram.Pages[0].PageSheet.PrintProps;

printProps.OnPage.Value = BOOL.True;

//Set Fit to sheet(s) across
printProps.PagesX.Value = 1;

//Set By sheet(s) down
printProps.PagesY.Value = 1;

{{< /highlight >}}
```


