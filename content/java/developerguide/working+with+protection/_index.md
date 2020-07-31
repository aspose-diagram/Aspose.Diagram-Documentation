---
title : "Working with Protection" 
description : "" 
weight : 8042 
toc : false
type: docs
url: /java/developerguide/working+with+protection/
---

# Aspose.Diagram for Java : Working with Protection


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Set Protection of the Visio Diagram](#set-protection-of-the-visio-diagram)
    *   1.1 [Edit Protection of the Visio Diagram](#edit-protection-of-the-visio-diagram)
    *   1.2 [Edit the Visio Shape Protection](#edit-the-visio-shape-protection)
{{< /panel >}}
 

 

## Set Protection of the Visio Diagram

Protecting diagrams allow users to lock backgrounds, masters (stencils), shapes and styles so that they cannot be edited. This is useful for protecting corporate styles, for example, and ensure a consistent look across a set of diagrams. Developers can achieve this using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java).

### Edit Protection of the Visio Diagram

The `getProtectBkgnds`, `getProtectMasters`, `getProtectShapes` and `getProtectStyles` methods, exposed by the [DocumentSettings](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/DocumentSettings) class support the `com.aspose.diagram.BoolValue` object. These properties can be used to protect and unprotect Microsoft Visio diagrams.

In Microsoft Visio you protect documents this way:

1.  Open a diagram in Microsoft Visio.
2.  Open Drawing Explorer window.
3.  Right click a diagram and select **Protect Document** from the menu.
4.  In the Protect Document window, check or clear options to lock or unlock different diagram elements.
5.  Click **OK**.

**Please see how we can check or clear options manually.**  
![](https://docs2.aspose.com/diagram/java/attachments/18612576/18809038.png)

Use the code below in a Java application to perform the same tasks – lock and unlock different elements of your diagram – using Aspose.Diagram for Java.

### Edit the Visio Shape Protection

Protecting Visio shapes allow users to lock specific aspects of shapes. Aspects of shapes that can be locked through shape protection include width, height, x-position, y-position, rotation and more. Developers can achieve this using [Aspose.Diagram for Java](https://products.aspose.com/diagram/java).

The **`getLockAspect()`**, **`getLockBegin()`**, **`getLockCalcWH()`**, **`getLockCrop()`**, **`getLockCustProp()`**, **`getLockDelete()`**, **`getLockEnd()`**, **`getLockFormat()`**, **`getLockFromGroupFormat()`**, **`getLockGroup()`**, **`getLockHeight()`**, **`getLockMoveX()`**, **`getLockMoveY()`**, **`getLockRotate()`**, **`getLockSelect()`**, **`getLockTextEdit()`**, **`getLockThemeColors()`**, **`getLockThemeEffects()`**, **`getLockVtxEdit()`** and **`getLockWidth()`** methods exposed by the [Protection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Protection) class support the `com.aspose.diagram.BoolValue` object. These methods can be used to protect/unprotect shapes.

In Visio, you need to perform following actions to protect any shape:

1.  Open a diagram in Microsoft Visio.
2.  Select a shape.
3.  Select **Protection** from the **Format** menu (Visio 2007), or select **Protection** from the **Developer** menu (Visio 2010).
4.  In the **Protection** window, select or clear options to lock or unlock shape attribute..
5.  Click **OK**.

**A shape's protection options, as seen in Microsoft Visio**  
![](https://docs2.aspose.com/diagram/java/attachments/18612576/18809039.png)

Use the following code in your Java application to do the same thing (lock/unlock any shape attribute) using Aspose.Diagram for Java.

