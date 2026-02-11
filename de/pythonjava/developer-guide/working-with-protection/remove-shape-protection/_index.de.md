---
title: Formschutz entfernen
type: docs
weight: 20
url: /de/python-java/remove-shape-protection/
description: This section explains how to remove shape protection using Aspose.Diagram for Python via Java.
---
## **Entfernen Sie den Schutz der Form Visio**
Protecting Visio shapes allow users to lock specific aspects of shapes. Aspects of shapes that can be locked through shape protection include width, height, x-position, y-position, rotation and more. Developers can achieve this using Aspose.Diagram for Python via Java.
### **Bearbeiten Sie den Formschutz Visio**
**LockAspect**, **LockBegin**, **LockCalcWH**, **LockCrop**, **LockCustProp**, **SperrenLöschen**, **LockEnd**, **LockFormat**, **LockFromGroupFormat**, **LockGroup**, **LockHeight**, **LockMoveX**, **LockMoveY**, **LockRotate**, **LockSelect**, **LockTextEdit**, **Themenfarben sperren**, **LockThemeEffects**, **LockVtxBearbeiten** und**Sperrbreite** Eigenschaften ausgesetzt durch**Schutz** Klasse unterstützt die**Aspose.Diagram.BoolValue** Objekt. Diese Eigenschaften können zum Schützen und Aufheben des Schutzes von Formen verwendet werden.

In Microsoft Office Visio kann der Benutzer die folgenden Aktionen ausführen, um jede Form zu schützen:

- Öffnen Sie diagram in Microsoft Office Visio
- Wählen Sie eine beliebige Form aus
- Wählen Sie „Schutz“ aus dem Menü „Format“, wenn Sie Visio 2007 verwenden, oder wählen Sie „Schutz“ aus dem Menü „Entwickler“, wenn Sie Visio 2010 verwenden
- Deaktivieren Sie im Fenster „Schutz“ alle Textfelder, um Formattribute zu entsperren
- Drücke OK'

### **Entfernen Sie das Shape Protection-Programmierbeispiel**
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


