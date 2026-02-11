---
title: Remove Shape Protection
type: docs
weight: 20
url: /python-java/remove-shape-protection/
description: This section explains how to remove shape protection using Aspose.Diagram for Python via Java.
---

## **Remove Protection of the Visio Shape**
Protecting Visio shapes allow users to lock specific aspects of shapes. Aspects of shapes that can be locked through shape protection include width, height, x-position, y-position, rotation and more. Developers can achieve this using Aspose.Diagram for Python via Java.
### **Edit the Visio Shape Protection**
**LockAspect**, **LockBegin**, **LockCalcWH**, **LockCrop**, **LockCustProp**, **LockDelete**, **LockEnd**, **LockFormat**, **LockFromGroupFormat**, **LockGroup**, **LockHeight**, **LockMoveX**, **LockMoveY**, **LockRotate**, **LockSelect**, **LockTextEdit**, **LockThemeColors**, **LockThemeEffects**, **LockVtxEdit** and **LockWidth** properties exposed by **Protection** class support the **Aspose.Diagram.BoolValue** object. These properties can be used to protect and unprotect shapes.

In Microsoft Office Visio, user may perform following actions to protect any shape:

- Open diagram in Microsoft Office Visio
- Select any shape
- Select 'Protection' from the 'Format' menu if you are using Visio 2007 or select 'Protection' from the 'Developer' menu if you are using Visio 2010
- In the 'Protection' window, uncheck any text box to unlock any shape attribute
- Press 'Ok'

### **Remove the Shape Protection Programming Sample**
Use the following code in your application to do the same thing (unlock any shape attribute) using Aspose.Diagram for Python via Java.


{{< highlight python >}}
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
shape.getProtection().getLockAspect().setValue(BOOL.FALSE)
shape.getProtection().getLockBegin().setValue(BOOL.FALSE)
shape.getProtection().getLockCalcWH().setValue(BOOL.FALSE)
shape.getProtection().getLockCrop().setValue(BOOL.FALSE)
shape.getProtection().getLockCustProp().setValue(BOOL.FALSE)
shape.getProtection().getLockDelete().setValue(BOOL.FALSE)
shape.getProtection().getLockEnd().setValue(BOOL.FALSE)
shape.getProtection().getLockFormat().setValue(BOOL.FALSE)
shape.getProtection().getLockFromGroupFormat().setValue(BOOL.FALSE)
shape.getProtection().getLockGroup().setValue(BOOL.FALSE)
shape.getProtection().getLockHeight().setValue(BOOL.FALSE)
shape.getProtection().getLockMoveX().setValue(BOOL.FALSE)
shape.getProtection().getLockMoveY().setValue(BOOL.FALSE)
shape.getProtection().getLockRotate().setValue(BOOL.FALSE)
shape.getProtection().getLockSelect().setValue(BOOL.FALSE)
shape.getProtection().getLockTextEdit().setValue(BOOL.FALSE)
shape.getProtection().getLockThemeColors().setValue(BOOL.FALSE)
shape.getProtection().getLockThemeEffects().setValue(BOOL.FALSE)
shape.getProtection().getLockVtxEdit().setValue(BOOL.FALSE)
shape.getProtection().getLockWidth().setValue(BOOL.FALSE)
        
# save diagram
diagram.save("VisioShapeProtection_Out.vsdx", SaveFileFormat.VSDX)
jpype.shutdownJVM()

{{< /highlight >}}


