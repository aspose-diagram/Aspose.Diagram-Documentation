---
title: Working with Protection
type: docs
weight: 90
url: /java/working-with-protection/
---

## **Set Protection of the Visio Diagram**
Protecting diagrams allow users to lock backgrounds, masters (stencils), shapes and styles so that they cannot be edited. This is useful for protecting corporate styles, for example, and ensure a consistent look across a set of diagrams. Developers can achieve this using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java).
### **Edit Protection of the Visio Diagram**
The getProtectBkgnds, getProtectMasters, getProtectShapes and getProtectStyles methods, exposed by the [DocumentSettings](https://apireference.aspose.com/diagram/java/com.aspose.diagram/DocumentSettings) class support the com.aspose.diagram.BoolValue object. These properties can be used to protect and unprotect Microsoft Visio diagrams.

In Microsoft Visio you protect documents this way:

1. Open a diagram in Microsoft Visio.
1. Open Drawing Explorer window.
1. Right click a diagram and select **Protect Document** from the menu.
1. In the Protect Document window, check or clear options to lock or unlock different diagram elements.
1. Click **OK**.

**Please see how we can check or clear options manually.** 

![todo:image_alt_text](working-with-protection_1.png)

Use the code below in a Java application to perform the same tasks – lock and unlock different elements of your diagram – using Aspose.Diagram for Java.

{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-Protection-VisioDiagramProtection-VisioDiagramProtection.java" >}}
### **Edit the Visio Shape Protection**
Protecting Visio shapes allow users to lock specific aspects of shapes. Aspects of shapes that can be locked through shape protection include width, height, x-position, y-position, rotation and more. Developers can achieve this using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java).

The **getLockAspect()**, **getLockBegin()**, **getLockCalcWH()**, **getLockCrop()**, **getLockCustProp()**, **getLockDelete()**, **getLockEnd()**, **getLockFormat()**, **getLockFromGroupFormat()**, **getLockGroup()**, **getLockHeight()**, **getLockMoveX()**, **getLockMoveY()**, **getLockRotate()**, **getLockSelect()**, **getLockTextEdit()**, **getLockThemeColors()**, **getLockThemeEffects()**, **getLockVtxEdit()** and **getLockWidth()** methods exposed by the [Protection](https://apireference.aspose.com/diagram/java/com.aspose.diagram/Protection) class support the com.aspose.diagram.BoolValue object. These methods can be used to protect/unprotect shapes.

In Visio, you need to perform following actions to protect any shape:

1. Open a diagram in Microsoft Visio.
1. Select a shape.
1. Select **Protection** from the **Format** menu (Visio 2007), or select **Protection** from the **Developer** menu (Visio 2010).
1. In the **Protection** window, select or clear options to lock or unlock shape attribute..
1. Click **OK**.

**A shape's protection options, as seen in Microsoft Visio** 

![todo:image_alt_text](working-with-protection_2.png)

Use the following code in your Java application to do the same thing (lock/unlock any shape attribute) using Aspose.Diagram for Java.

{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-Protection-VisioShapeProtection-VisioShapeProtection.java" >}}
