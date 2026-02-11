---
title: 使用保护
type: docs
weight: 170
url: /zh/net/working-with-protection/
description: 本节介绍如何在 diagram 和 Aspose.Diagram 中设置保护。
---
## **设置保护 Visio Diagram**
保护图表允许用户锁定背景、母版（模板）、形状和样式，使它们无法被编辑。这对于保护公司风格很有用，例如，并确保一组图表的外观一致。开发人员可以使用[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **编辑 Visio Diagram 保护**
ProtectBkgnds、ProtectMasters、ProtectShapes 和 ProtectStyles 属性，由[文档设置](http://www.aspose.com/api/net/diagram/aspose.diagram/documentsettings)类支持 Aspose.Diagram.BoolValue 对象。这些属性可用于保护和取消保护 Microsoft Office Visio 图。在 Microsoft Visio 中，您以这种方式保护文档：

1. 在Microsoft Visio开一个diagram。
1. 打开绘图资源管理器窗口。
1. 右键单击 diagram 并选择**保护文档**从菜单中。
1. 在“保护文档”窗口中，选中或清除选项以锁定或解锁不同的 diagram 元素。
1. 点击**好的**.
#### **编辑 Diagram 保护编程示例**
在 .NET 应用程序中使用以下代码执行相同的任务，例如使用 Aspose.Diagram for .NET API 锁定和解锁 Visio diagram 的不同元素。

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Protection();

// Load diagram
Diagram diagram = new Diagram(dataDir + "ProtectAndUnprotect.vsd");

diagram.DocumentSettings.ProtectBkgnds = BOOL.True;
diagram.DocumentSettings.ProtectMasters = BOOL.True;
diagram.DocumentSettings.ProtectShapes = BOOL.True;
diagram.DocumentSettings.ProtectStyles = BOOL.True;
// Save diagram
diagram.Save(dataDir + "VisioDiagramProtection_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **设置Visio形状的保护**
保护 Visio 形状允许用户锁定形状的特定方面。可以通过形状保护锁定的形状方面包括宽度、高度、x 位置、y 位置、旋转等。开发人员可以使用[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **编辑Visio形状保护**
**锁定画面**, **锁定开始**, **锁定计算器WH**, **锁定裁剪**, **LockCustProp**, **锁定删除**, **锁定结束**, **锁定格式**, **LockFromGroupFormat**, **锁组**, **锁定高度**, **锁定移动X**, **锁定移动Y**, **锁定旋转**, **锁定选择**, **LockText编辑**, **锁定主题颜色**, **锁定主题效果**, **LockVtx编辑**和**锁定宽度**暴露的属性[**保护**](http://www.aspose.com/api/net/diagram/aspose.diagram/Protection)类支持**Aspose.Diagram.BoolValue**目的。这些属性可用于保护和取消保护形状。

在 Microsoft Office Visio 中，用户可以执行以下操作来保护任何形状：

- 在 Microsoft Office Visio 打开 diagram
- 选择任意形状
- 如果您使用的是 Visio 2007，请从“格式”菜单中选择“保护...”；如果您使用的是 Visio 2010，请从“开发人员”菜单中选择“保护”
- 在“保护”窗口中，选中/取消选中任何文本框以锁定或解锁任何形状属性
- 按“确定”
### **编辑形状保护编程示例**
在您的 .NET 应用程序中使用以下代码来使用 Aspose.Diagram for .NET 执行相同的操作（锁定/解锁任何形状属性）。

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Protection();

// Load diagram
Diagram diagram = new Diagram(dataDir + "ProtectAndUnprotect.vsd");
// Get page by name
Page page = diagram.Pages.GetPage("Flow 1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);

// Set protections
shape.Protection.LockAspect.Value = BOOL.True;
shape.Protection.LockBegin.Value = BOOL.True;
shape.Protection.LockCalcWH.Value = BOOL.True;
shape.Protection.LockCrop.Value = BOOL.True;
shape.Protection.LockCustProp.Value = BOOL.True;
shape.Protection.LockDelete.Value = BOOL.True;
shape.Protection.LockEnd.Value = BOOL.True;
shape.Protection.LockFormat.Value = BOOL.True;
shape.Protection.LockFromGroupFormat.Value = BOOL.True;
shape.Protection.LockGroup.Value = BOOL.True;
shape.Protection.LockHeight.Value = BOOL.True;
shape.Protection.LockMoveX.Value = BOOL.True;
shape.Protection.LockMoveY.Value = BOOL.True;
shape.Protection.LockRotate.Value = BOOL.True;
shape.Protection.LockSelect.Value = BOOL.True;
shape.Protection.LockTextEdit.Value = BOOL.True;
shape.Protection.LockThemeColors.Value = BOOL.True;
shape.Protection.LockThemeEffects.Value = BOOL.True;
shape.Protection.LockVtxEdit.Value = BOOL.True;
shape.Protection.LockWidth.Value = BOOL.True;
            
// Save diagram
diagram.Save(dataDir + "VisioShapeProtection_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
