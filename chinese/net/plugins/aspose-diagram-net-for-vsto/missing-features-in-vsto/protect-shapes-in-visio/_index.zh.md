---
title: 保护 Visio 中的形状
type: docs
weight: 20
url: /zh/net/protect-shapes-in-visio/
---
LockAspect、LockBegin、LockCalcWH、LockCrop、LockCustProp、LockDelete、LockEnd、LockFormat、LockFromGroupFormat、LockGroup、LockHeight、LockMoveX、LockMoveY、LockRotate、LockSelect、LockTextEdit、LockThemeColors、LockThemeEffects、LockVtxEdit 和 LockWidth Protection 类公开的属性支持 Aspose.Diagram.BoolValue 对象.这些属性可用于保护/取消保护形状。

在 Visio 中，您需要执行以下操作来保护任何形状：

- 在 MS Visio 中打开 diagram
- 选择任意形状
- 如果您使用的是 Visio 2007，请从“格式”菜单中选择“保护...”；如果您使用的是 Visio 2010，请从“开发人员”菜单中选择“保护”
- 在“保护”窗口中，选中/取消选中任何文本框以锁定或解锁任何形状属性
- 按“确定”

在您的 .NET 应用程序中使用以下代码使用 Aspose.Diagram for .NET 执行相同的操作（锁定任何形状属性）。

{{< highlight "csharp" >}}

 //Load diagram

Diagram diagram = new Diagram("ProtectShape.vsd");

Page page0 = diagram.Pages[0];

Shape shape = page0.Shapes[0];

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

diagram.Save("ProtectedShapesFile.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
## **下载示例代码**
- [比特桶](https://bitbucket.org/asposemarketplace/aspose-for-vsto/src/master/Aspose.Diagram%20Vs%20VSTO%20Visio/)
