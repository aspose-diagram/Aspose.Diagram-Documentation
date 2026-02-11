---
title: 移除形状保护
type: docs
weight: 20
url: /zh/net/remove-shape-protection/
description: 本节介绍如何移除形状保护。
---
## **移除 Visio 形状的保护**
保护 Visio 形状允许用户锁定形状的特定方面。可以通过形状保护锁定的形状方面包括宽度、高度、x 位置、y 位置、旋转等。开发人员可以使用[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **编辑Visio形状保护**
**锁定画面**, **锁定开始**, **锁定计算器WH**, **锁定裁剪**, **LockCustProp**, **锁定删除**, **锁定结束**, **锁定格式**, **LockFromGroupFormat**, **锁组**, **锁定高度**, **锁定移动X**, **锁定移动Y**, **锁定旋转**, **锁定选择**, **LockText编辑**, **锁定主题颜色**, **锁定主题效果**, **LockVtx编辑**和**锁定宽度**暴露的属性[**保护**](http://www.aspose.com/api/net/diagram/aspose.diagram/Protection)类支持**Aspose.Diagram.BoolValue**目的。这些属性可用于保护和取消保护形状。

在 Microsoft Office Visio 中，用户可以执行以下操作来保护任何形状：

- 在 Microsoft Office Visio 打开 diagram
- 选择任意形状
- 如果您使用的是 Visio 2007，请从“格式”菜单中选择“保护”；如果您使用的是 Visio 2010，请从“开发人员”菜单中选择“保护”
- 在“保护”窗口中，取消选中任何文本框以解锁任何形状属性
- 按“确定”
### **删除形状保护编程示例**
在您的 .NET 应用程序中使用以下代码使用 Aspose.Diagram for .NET 执行相同的操作（解锁任何形状属性）。


{{< highlight csharp >}}
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
shape.Protection.LockAspect.Value = BOOL.False;
shape.Protection.LockBegin.Value = BOOL.False;
shape.Protection.LockCalcWH.Value = BOOL.False;
shape.Protection.LockCrop.Value = BOOL.False;
shape.Protection.LockCustProp.Value = BOOL.False;
shape.Protection.LockDelete.Value = BOOL.False;
shape.Protection.LockEnd.Value = BOOL.False;
shape.Protection.LockFormat.Value = BOOL.False;
shape.Protection.LockFromGroupFormat.Value = BOOL.False;
shape.Protection.LockGroup.Value = BOOL.False;
shape.Protection.LockHeight.Value = BOOL.False;
shape.Protection.LockMoveX.Value = BOOL.False;
shape.Protection.LockMoveY.Value = BOOL.False;
shape.Protection.LockRotate.Value = BOOL.False;
shape.Protection.LockSelect.Value = BOOL.False;
shape.Protection.LockTextEdit.Value = BOOL.False;
shape.Protection.LockThemeColors.Value = BOOL.False;
shape.Protection.LockThemeEffects.Value = BOOL.False;
shape.Protection.LockVtxEdit.Value = BOOL.False;
shape.Protection.LockWidth.Value = BOOL.False;
            
// Save diagram
diagram.Save(dataDir + "RemoveShapeProtection_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

