---
title: Protect Shapes in Visio
type: docs
weight: 20
url: /net/protect-shapes-in-visio/
---

LockAspect, LockBegin, LockCalcWH, LockCrop, LockCustProp, LockDelete, LockEnd, LockFormat, LockFromGroupFormat, LockGroup, LockHeight, LockMoveX, LockMoveY, LockRotate, LockSelect, LockTextEdit, LockThemeColors, LockThemeEffects, LockVtxEdit and LockWidth properties exposed by Protection class support the Aspose.Diagram.BoolValue object. These properties can be used to protect/unprotect shapes.

In Visio, you need to perform following actions to protect any shape:

- Open diagram in MS Visio
- Select any shape
- Select ‘Protection…’ from the ‘Format’ menu if you are using Visio 2007 or select ‘Protection’ from the ‘Developer’ menu if you are using Visio 2010
- In the ‘Protection’ window, check/uncheck any text box to lock or unlock any shape attribute
- Press ‘Ok’

Use the following code in your .NET application to do the same thing (lock any shape attribute) using Aspose.Diagram for .NET.

{{< highlight csharp >}}

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
## **Download Sample Code**
- [Bitbucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/downloads/ProtectUnprotectShapes%20%28Aspose.Diagram%29.zip)
