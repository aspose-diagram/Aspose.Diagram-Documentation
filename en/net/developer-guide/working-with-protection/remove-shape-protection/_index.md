---
title: Remove Shape Protection
type: docs
weight: 20
url: /net/remove-shape-protection/
description: This section explains how to remove shape protection.
---

## **Remove Protection of the Visio Shape**
Protecting Visio shapes allow users to lock specific aspects of shapes. Aspects of shapes that can be locked through shape protection include width, height, x-position, y-position, rotation and more. Developers can achieve this using [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Edit the Visio Shape Protection**
**LockAspect**, **LockBegin**, **LockCalcWH**, **LockCrop**, **LockCustProp**, **LockDelete**, **LockEnd**, **LockFormat**, **LockFromGroupFormat**, **LockGroup**, **LockHeight**, **LockMoveX**, **LockMoveY**, **LockRotate**, **LockSelect**, **LockTextEdit**, **LockThemeColors**, **LockThemeEffects**, **LockVtxEdit** and **LockWidth** properties exposed by [**Protection**](http://www.aspose.com/api/net/diagram/aspose.diagram/Protection) class support the **Aspose.Diagram.BoolValue** object. These properties can be used to protect and unprotect shapes.

In Microsoft Office Visio, user may perform following actions to protect any shape:

- Open diagram in Microsoft Office Visio
- Select any shape
- Select 'Protection' from the 'Format' menu if you are using Visio 2007 or select 'Protection' from the 'Developer' menu if you are using Visio 2010
- In the 'Protection' window, uncheck any text box to unlock any shape attribute
- Press 'Ok'
### **Remove the Shape Protection Programming Sample**
Use the following code in your .NET application to do the same thing (unlock any shape attribute) using Aspose.Diagram for .NET.

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
```
