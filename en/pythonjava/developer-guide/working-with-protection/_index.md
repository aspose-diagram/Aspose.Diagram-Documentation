---
title: Working with Protection
type: docs
weight: 90
url: /python-java/working-with-protection/
---

## **Set Protection of the Visio Diagram**
Protecting diagrams allow users to lock backgrounds, masters (stencils), shapes and styles so that they cannot be edited. This is useful for protecting corporate styles, for example, and ensure a consistent look across a set of diagrams. Developers can achieve this using Aspose.Diagram for Python via Java.

### **Edit Protection of the Visio Diagram**
The getProtectBkgnds, getProtectMasters, getProtectShapes and getProtectStyles methods, exposed by the DocumentSettings class support the BoolValue object. These properties can be used to protect and unprotect Microsoft Visio diagrams.

In Microsoft Visio you protect documents this way:

1. Open a diagram in Microsoft Visio.
1. Open Drawing Explorer window.
1. Right click a diagram and select **Protect Document** from the menu.
1. In the Protect Document window, check or clear options to lock or unlock different diagram elements.
1. Click **OK**.

**Please see how we can check or clear options manually.** 

Use the code below in your application to perform the same tasks – lock and unlock different elements of your diagram – using Aspose.Diagram for Python via Java.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Load diagram
diagram = Diagram("ProtectAndUnprotect.vsd")

diagram.getDocumentSettings().setProtectBkgnds(BOOL.TRUE)
diagram.getDocumentSettings().setProtectMasters(BOOL.TRUE)
diagram.getDocumentSettings().setProtectShapes(BOOL.TRUE)
diagram.getDocumentSettings().setProtectStyles(BOOL.TRUE)

# save diagram
diagram.save("VisioDiagramProtection_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```

### **Edit the Visio Shape Protection**
Protecting Visio shapes allow users to lock specific aspects of shapes. Aspects of shapes that can be locked through shape protection include width, height, x-position, y-position, rotation and more. Developers can achieve this using Aspose.Diagram for Python via Java.

The **getLockAspect()**, **getLockBegin()**, **getLockCalcWH()**, **getLockCrop()**, **getLockCustProp()**, **getLockDelete()**, **getLockEnd()**, **getLockFormat()**, **getLockFromGroupFormat()**, **getLockGroup()**, **getLockHeight()**, **getLockMoveX()**, **getLockMoveY()**, **getLockRotate()**, **getLockSelect()**, **getLockTextEdit()**, **getLockThemeColors()**, **getLockThemeEffects()**, **getLockVtxEdit()** and **getLockWidth()** methods exposed by the **Protection** class support the BoolValue object. These methods can be used to protect/unprotect shapes.

In Visio, you need to perform following actions to protect any shape:

1. Open a diagram in Microsoft Visio.
1. Select a shape.
1. Select **Protection** from the **Format** menu (Visio 2007), or select **Protection** from the **Developer** menu (Visio 2010).
1. In the **Protection** window, select or clear options to lock or unlock shape attribute..
1. Click **OK**.

**A shape\'s protection options, as seen in Microsoft Visio** 

Use the following code in your Java application to do the same thing (lock/unlock any shape attribute) using Aspose.Diagram for Python via Java.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Load diagram
diagram = Diagram("ProtectAndUnprotect.vsd")
# get page by name
page = diagram.getPages().getPage("Flow 1")
# get shape by ID
shape = page.getShapes().getShape(1)

# set protections
shape.getProtection().getLockAspect().setValue(BOOL.TRUE)
shape.getProtection().getLockBegin().setValue(BOOL.TRUE)
shape.getProtection().getLockCalcWH().setValue(BOOL.TRUE)
shape.getProtection().getLockCrop().setValue(BOOL.TRUE)
shape.getProtection().getLockCustProp().setValue(BOOL.TRUE)
shape.getProtection().getLockDelete().setValue(BOOL.TRUE)
shape.getProtection().getLockEnd().setValue(BOOL.TRUE)
shape.getProtection().getLockFormat().setValue(BOOL.TRUE)
shape.getProtection().getLockFromGroupFormat().setValue(BOOL.TRUE)
shape.getProtection().getLockGroup().setValue(BOOL.TRUE)
shape.getProtection().getLockHeight().setValue(BOOL.TRUE)
shape.getProtection().getLockMoveX().setValue(BOOL.TRUE)
shape.getProtection().getLockMoveY().setValue(BOOL.TRUE)
shape.getProtection().getLockRotate().setValue(BOOL.TRUE)
shape.getProtection().getLockSelect().setValue(BOOL.TRUE)
shape.getProtection().getLockTextEdit().setValue(BOOL.TRUE)
shape.getProtection().getLockThemeColors().setValue(BOOL.TRUE)
shape.getProtection().getLockThemeEffects().setValue(BOOL.TRUE)
shape.getProtection().getLockVtxEdit().setValue(BOOL.TRUE)
shape.getProtection().getLockWidth().setValue(BOOL.TRUE)
        
# save diagram
diagram.save("VisioShapeProtection_Out.vdx", SaveFileFormat.VDX)
jpype.shutdownJVM()

{{< /highlight >}}
```
