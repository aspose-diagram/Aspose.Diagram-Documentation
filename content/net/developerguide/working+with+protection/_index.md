---
title : "Working with Protection" 
description : "" 
weight : 8049 
toc : false
type: docs
url: /net/developerguide/working+with+protection/
---

# Aspose.Diagram for .NET : Working with Protection


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Set Protection of the Visio Diagram](#set-protection-of-the-visio-diagram)
    *   1.1 [Edit the Visio Diagram Protection](#edit-the-visio-diagram-protection)
        *   1.1.1 [Edit the Diagram Protection Programming Sample](#edit-the-diagram-protection-programming-sample)
*   2 [Set Protection of the Visio Shape](#set-protection-of-the-visio-shape)
    *   2.1 [Edit the Visio Shape Protection](#edit-the-visio-shape-protection)
    *   2.2 [Edit the Shape Protection Programming Sample](#edit-the-shape-protection-programming-sample)
{{< /panel >}}
 

 

## Set Protection of the Visio Diagram

Protecting diagrams allow users to lock backgrounds, masters (stencils), shapes and styles so that they cannot be edited. This is useful for protecting corporate styles, for example, and ensure a consistent look across a set of diagrams. Developers can achieve this using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx).

### Edit the Visio Diagram Protection

The `ProtectBkgnds`, `ProtectMasters`, `ProtectShapes` and `ProtectStyles` properties, exposed by the [DocumentSettings](http://www.aspose.com/api/net/diagram/aspose.diagram/documentsettings) class support the `Aspose.Diagram.BoolValue` object. These properties can be used to protect and unprotect Microsoft Office Visio diagrams. In Microsoft Visio you protect documents in this way:

1.  Open a diagram in Microsoft Visio.
2.  Open Drawing Explorer window.
3.  Right click a diagram and select **Protect Document** from the menu.
4.  In the Protect Document window, check or clear options to lock or unlock different diagram elements.
5.  Click **OK**.

#### Edit the Diagram Protection Programming Sample

Use the code below in a .NET application to perform the same tasks like lock and unlock different elements of the Visio diagram using Aspose.Diagram for .NET API.

## Set Protection of the Visio Shape

Protecting Visio shapes allow users to lock specific aspects of shapes. Aspects of shapes that can be locked through shape protection include width, height, x-position, y-position, rotation and more. Developers can achieve this using [Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx).

### Edit the Visio Shape Protection

**LockAspect**, **LockBegin**, **LockCalcWH**, **LockCrop**, **LockCustProp**, **LockDelete**, **LockEnd**, **LockFormat**, **LockFromGroupFormat**, **LockGroup**, **LockHeight**, **LockMoveX**, **LockMoveY**, **LockRotate**, **LockSelect**, **LockTextEdit**, **LockThemeColors**, **LockThemeEffects**, **LockVtxEdit** and **LockWidth** properties exposed by **[Protection](http://www.aspose.com/api/net/diagram/aspose.diagram/Protection)** class support the **Aspose.Diagram.BoolValue** object. These properties can be used to protect and unprotect shapes.

In Microsoft Office Visio, user may perform following actions to protect any shape:

*   Open diagram in Microsoft Office Visio
*   Select any shape
*   Select ‘Protection…’ from the ‘Format’ menu if you are using Visio 2007 or select ‘Protection’ from the ‘Developer’ menu if you are using Visio 2010
*   In the ‘Protection’ window, check/uncheck any text box to lock or unlock any shape attribute
*   Press ‘Ok’

### Edit the Shape Protection Programming Sample

Use the following code in your .NET application to do the same thing (lock/unlock any shape attribute) using Aspose.Diagram for .NET.

