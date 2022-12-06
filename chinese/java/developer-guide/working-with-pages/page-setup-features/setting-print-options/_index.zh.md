---
title: 设置打印选项
type: docs
weight: 10
url: /zh/java/setting-print-options/
description: 本节介绍如何使用 Aspose.Diagram 设置打印选项。
---
{{% alert color="primary" %}}

有时，需要为页面配置页面设置以控制打印。这些页面设置设置提供了各种选项。

{{% /alert %}}

## **设置打印选项**

Aspose.Diagram 完全支持页面设置选项。本文介绍了如何使用 Aspose.Diagram 设置页面选项，并显示了用于设置的代码示例：

 Aspose.Diagram提供了一个类，[**页**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) ，代表一个 Microsoft Visio 文件。这[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)类包含一个[**页数**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagecollection)允许访问 Visio 文件中每个页面的集合。一个页面由[**页**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)班级。

这[**页表**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet)类提供了[**打印道具**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps)用于设置页面的页面设置选项的属性。事实上，这[**打印道具**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps)属性是[**页表**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet)用于为打印页面设置不同页面布局选项的类。这[**打印道具**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps)类提供用于设置页面设置选项的各种属性。下面讨论其中一些特性。

### **打印页面方向**

打印页面方向可以设置为纵向或横向使用[**打印道具**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagesheet#PrintProps)班级'[**打印页面方向**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PrintPageOrientation)财产。这[**打印页面方向**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#PrintPageOrientation)属性接受中的预定义值之一[**打印页面方向值**](https://reference.aspose.com/diagram/java/com.aspose.diagram/PrintPageOrientationValue)枚举，如下所示。

|**打印页面方向类型**|**描述**|
|:- |:- |
|与打印机相同|与打印机方向相同|
|景观|横向|
|肖像|纵向|

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Print-SetPageOrientation-SetPageOrientation.java" >}}

### **比例因子**

可以通过调整比例因子来缩小或放大页面的大小[**秤X**](https://reference.aspose.com/diagram/java/com.aspose.diagram/printprops#ScaleX)财产。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Print-SetPageOrientation-SetPageScale.java" >}}
