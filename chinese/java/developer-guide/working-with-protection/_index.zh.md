---
title: 使用保护
type: docs
weight: 90
url: /zh/java/working-with-protection/
---
## **设置保护 Visio Diagram**
保护图表允许用户锁定背景、母版（模板）、形状和样式，使它们无法被编辑。这对于保护公司风格很有用，例如，并确保一组图表的外观一致。开发人员可以使用[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).
### **编辑保护Visio Diagram**
 getProtectBkgnds、getProtectMasters、getProtectShapes 和 getProtectStyles 方法，由[文档设置](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentSettings)类支持 com.aspose.diagram.BoolValue 对象。这些属性可用于保护和取消保护 Microsoft Visio 图。

在 Microsoft Visio 中，您以这种方式保护文档：

1. 在Microsoft Visio开一个diagram。
1. 打开绘图资源管理器窗口。
1. 右键单击 diagram 并选择**保护文档**从菜单中。
1. 在“保护文档”窗口中，选中或清除选项以锁定或解锁不同的 diagram 元素。
1. 点击**好的**.

**请查看我们如何手动检查或清除选项。** 

![待办事项：图片_替代_文本](working-with-protection_1.png)

在 Java 应用程序中使用以下代码执行相同的任务 – 锁定和解锁 diagram 的不同元素 – 使用 Aspose.Diagram for Java。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Protection-VisioDiagramProtection-VisioDiagramProtection.java" >}}
### **编辑Visio形状保护**
保护 Visio 形状允许用户锁定形状的特定方面。可以通过形状保护锁定的形状方面包括宽度、高度、x 位置、y 位置、旋转等。开发人员可以使用[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

这**getLockAspect（）**, **获取锁定开始()**, **getLockCalcWH()**, **getLockCrop()**, **getLockCustProp()**, **获取锁定删除()**, **getLockEnd()**, **获取锁定格式()**, **getLockFromGroupFormat()**, **getLockGroup()**, **获取锁定高度()**, **getLockMoveX（）**, **getLockMoveY（）**, **getLockRotate() 方法**, **获取锁定选择()**, **获取锁定文本编辑()**, **getLockThemeColors（）**, **getLockThemeEffects() 方法**, **getLockVtxEdit()**和**获取锁定宽度()**公开的方法[保护](https://reference.aspose.com/diagram/java/com.aspose.diagram/Protection)类支持 com.aspose.diagram.BoolValue 对象。这些方法可用于保护/取消保护形状。

在 Visio 中，您需要执行以下操作来保护任何形状：

1. 在Microsoft Visio开一个diagram。
1. 选择一个形状。
1. 选择**保护**来自**格式**菜单 (Visio 2007)，或选择**保护**来自**开发商**菜单（Visio 2010）。
1. 在里面**保护**窗口，选择或清除选项以锁定或解锁形状属性。
1. 点击**好的**.

**形状的保护选项，如 Microsoft Visio 所示** 

![待办事项：图片_替代_文本](working-with-protection_2.png)

在您的 Java 应用程序中使用以下代码来使用 Aspose.Diagram for Java 执行相同的操作（锁定/解锁任何形状属性）。

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Protection-VisioShapeProtection-VisioShapeProtection.java" >}}
