---
title: Rimuovi la protezione della forma
type: docs
weight: 20
url: /it/python-java/remove-shape-protection/
description: This section explains how to remove shape protection using Aspose.Diagram for Python via Java.
---
## **Rimuovere la protezione della forma Visio**
Protecting Visio shapes allow users to lock specific aspects of shapes. Aspects of shapes that can be locked through shape protection include width, height, x-position, y-position, rotation and more. Developers can achieve this using Aspose.Diagram for Python via Java.
### **Modifica la protezione della forma Visio**
**LockAspect**, **LockBegin**, **LockCalc WH**, **LockCrop**, **LockCustProp**, **BloccaElimina**, **LockEnd**, **BloccaFormat**, **LockFromGroupFormat**, **Gruppo di blocco**, **LockHeight**, **LockMoveX**, **LockMoveY**, **Blocca Ruota**, **BloccaSeleziona**, **LockTextModifica**, **LockThemeColors**, **LockThemeEffects**, **LockVtxModifica** e**LockWidth** proprietà esposte da**Protezione** classe sostenere il**Aspose.Diagram.BoolValue** oggetto. Queste proprietà possono essere utilizzate per proteggere e rimuovere la protezione delle forme.

In Microsoft Office Visio, l'utente può eseguire le seguenti azioni per proteggere qualsiasi forma:

- Aperto diagram in Microsoft Office Visio
- Seleziona qualsiasi forma
- Selezionare 'Protezione' dal menu 'Formato' se si utilizza Visio 2007 o selezionare 'Protezione' dal menu 'Sviluppatore' se si utilizza Visio 2010
- Nella finestra "Protezione", deseleziona qualsiasi casella di testo per sbloccare qualsiasi attributo della forma
- Premere OK'

### **Rimuovi l'esempio di programmazione di Shape Protection**
Use the following code in your application to do the same thing (unlock any shape attribute) using Aspose.Diagram for Python via Java.

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
```

