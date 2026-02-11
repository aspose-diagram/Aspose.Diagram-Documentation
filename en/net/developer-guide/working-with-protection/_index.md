---
title: Working with Protection
type: docs
weight: 170
url: /net/working-with-protection/
description: This section explains how to set protection in the diagram with Aspose.Diagram.
---

## **Set Protection of the Visio Diagram**
Protecting diagrams allow users to lock backgrounds, masters (stencils), shapes and styles so that they cannot be edited. This is useful for protecting corporate styles, for example, and ensure a consistent look across a set of diagrams. Developers can achieve this using [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Edit the Visio Diagram Protection**
The ProtectBkgnds, ProtectMasters, ProtectShapes and ProtectStyles properties, exposed by the [DocumentSettings](http://www.aspose.com/api/net/diagram/aspose.diagram/documentsettings) class support the Aspose.Diagram.BoolValue object. These properties can be used to protect and unprotect Microsoft Office Visio diagrams. In Microsoft Visio you protect documents in this way:

1. Open a diagram in Microsoft Visio.
1. Open Drawing Explorer window.
1. Right click a diagram and select **Protect Document** from the menu.
1. In the Protect Document window, check or clear options to lock or unlock different diagram elements.
1. Click **OK**.
#### **Edit the Diagram Protection Programming Sample**
Use the code below in a .NET application to perform the same tasks like lock and unlock different elements of the Visio diagram using Aspose.Diagram for .NET API.


{{< highlight csharp >}}
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

## **Set Protection of the Visio Shape**
Protecting Visio shapes allow users to lock specific aspects of shapes. Aspects of shapes that can be locked through shape protection include width, height, x-position, y-position, rotation and more. Developers can achieve this using [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Edit the Visio Shape Protection**
**LockAspect**, **LockBegin**, **LockCalcWH**, **LockCrop**, **LockCustProp**, **LockDelete**, **LockEnd**, **LockFormat**, **LockFromGroupFormat**, **LockGroup**, **LockHeight**, **LockMoveX**, **LockMoveY**, **LockRotate**, **LockSelect**, **LockTextEdit**, **LockThemeColors**, **LockThemeEffects**, **LockVtxEdit** and **LockWidth** properties exposed by [**Protection**](http://www.aspose.com/api/net/diagram/aspose.diagram/Protection) class support the **Aspose.Diagram.BoolValue** object. These properties can be used to protect and unprotect shapes.

In Microsoft Office Visio, user may perform following actions to protect any shape:

- Open diagram in Microsoft Office Visio
- Select any shape
- Select ‘Protection…’ from the ‘Format’ menu if you are using Visio 2007 or select ‘Protection’ from the ‘Developer’ menu if you are using Visio 2010
- In the ‘Protection’ window, check/uncheck any text box to lock or unlock any shape attribute
- Press ‘Ok’
### **Edit the Shape Protection Programming Sample**
Use the following code in your .NET application to do the same thing (lock/unlock any shape attribute) using Aspose.Diagram for .NET.


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

