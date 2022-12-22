---
title: 设置边距
type: docs
weight: 20
url: /zh/net/setting-margins/
description: 本节介绍如何使用 Aspose.Diagram 设置 visio 的页面选项。
---
{{% alert color="primary" %}}

Aspose.Diagram 完全支持 Microsoft Visio 的页面设置选项。开发人员可能需要为页面配置页面设置以控制打印过程。本主题讨论如何使用 Aspose.Diagram 配置页边距。

{{% /alert %}}

## **设置边距**

 Aspose.Diagram提供了一个类，[**页**](https://reference.aspose.com/diagram/net/aspose.diagram/page) ，代表一个 Microsoft Visio 文件。这[**Diagram**](https://reference.aspose.com/diagram/net/aspose.diagram/page)类包含一个[**页数**](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection)允许访问 Visio 文件中每个页面的集合。一个页面由[**页**](https://reference.aspose.com/diagram/net/aspose.diagram/page)班级。

这[**页表**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet)类提供了[**打印道具**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)用于设置页面的页面设置选项的属性。事实上，这[**打印道具**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)属性是[**页表**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet)用于为打印页面设置不同页面布局选项的类。这[**打印道具**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)类提供用于设置页面设置选项的各种属性。下面讨论其中一些特性。

### **页边距**

使用设置页边距（PageTopMargin、PageBottomMargin、PageLeftMargin、PageRightMargin）[**打印道具**](https://reference.aspose.com/diagram/net/aspose.diagram/pagesheet/properties/printprops)班级成员。下面列出了一些用于指定页边距的方法：

- [**PageTopMargin**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagetopmargin)
- [**页底边距**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagebottommargin)
- [**左页边距**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pageleftmargin)
- [**页右边距**](https://reference.aspose.com/diagram/net/aspose.diagram/printprops/properties/pagerightmargin)

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-SetPageMargin-SetPageMargin.cs" >}}