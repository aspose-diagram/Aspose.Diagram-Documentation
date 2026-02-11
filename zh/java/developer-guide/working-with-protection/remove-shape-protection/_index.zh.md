---
title: 移除形状保护
type: docs
weight: 20
url: /zh/java/remove-shape-protection/
description: 本节介绍如何使用 Aspose.Diagram 移除形状保护。
---
## **移除 Visio 形状的保护**
保护 Visio 形状允许用户锁定形状的特定方面。可以通过形状保护锁定的形状方面包括宽度、高度、x 位置、y 位置、旋转等。开发人员可以使用[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).
### **编辑Visio形状保护**
**锁定画面**, **锁定开始**, **锁定计算器WH**, **锁定裁剪**, **LockCustProp**, **锁定删除**, **锁定结束**, **锁定格式**, **LockFromGroupFormat**, **锁组**, **锁定高度**, **锁定移动X**, **锁定移动Y**, **锁定旋转**, **锁定选择**, **LockText编辑**, **锁定主题颜色**, **锁定主题效果**, **LockVtx编辑**和**锁定宽度**暴露的属性[**保护**](https://reference.aspose.com/diagram/java/com.aspose.diagram/protection)类支持**Aspose.Diagram.BoolValue**目的。这些属性可用于保护和取消保护形状。

在 Microsoft Office Visio 中，用户可以执行以下操作来保护任何形状：

- 在 Microsoft Office Visio 打开 diagram
- 选择任意形状
- 如果您使用的是 Visio 2007，请从“格式”菜单中选择“保护”；如果您使用的是 Visio 2010，请从“开发人员”菜单中选择“保护”
- 在“保护”窗口中，取消选中任何文本框以解锁任何形状属性
- 按“确定”
### **删除形状保护编程示例**
在您的 Java 应用程序中使用以下代码使用 Aspose.Diagram for Java 执行相同的操作（解锁任何形状属性）。

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VisioShapeProtection.class);
//Load diagram
Diagram diagram = new Diagram(dataDir + "ProtectAndUnprotect.vsd");
// get page by name
Page page = diagram.getPages().getPage("Flow 1");
// get shape by ID
Shape shape = page.getShapes().getShape(1);

// set protections
shape.getProtection().getLockAspect().setValue(BOOL.FALSE);
shape.getProtection().getLockBegin().setValue(BOOL.FALSE);
shape.getProtection().getLockCalcWH().setValue(BOOL.FALSE);
shape.getProtection().getLockCrop().setValue(BOOL.FALSE);
shape.getProtection().getLockCustProp().setValue(BOOL.FALSE);
shape.getProtection().getLockDelete().setValue(BOOL.FALSE);
shape.getProtection().getLockEnd().setValue(BOOL.FALSE);
shape.getProtection().getLockFormat().setValue(BOOL.FALSE);
shape.getProtection().getLockFromGroupFormat().setValue(BOOL.FALSE);
shape.getProtection().getLockGroup().setValue(BOOL.FALSE);
shape.getProtection().getLockHeight().setValue(BOOL.FALSE);
shape.getProtection().getLockMoveX().setValue(BOOL.FALSE);
shape.getProtection().getLockMoveY().setValue(BOOL.FALSE);
shape.getProtection().getLockRotate().setValue(BOOL.FALSE);
shape.getProtection().getLockSelect().setValue(BOOL.FALSE);
shape.getProtection().getLockTextEdit().setValue(BOOL.FALSE);
shape.getProtection().getLockThemeColors().setValue(BOOL.FALSE);
shape.getProtection().getLockThemeEffects().setValue(BOOL.FALSE);
shape.getProtection().getLockVtxEdit().setValue(BOOL.FALSE);
shape.getProtection().getLockWidth().setValue(BOOL.FALSE);
        
// save diagram
diagram.save(dataDir + "VisioShapeProtection_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

