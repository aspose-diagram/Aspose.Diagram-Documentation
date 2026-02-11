---
title: Eliminar protección de forma
type: docs
weight: 20
url: /es/python-java/remove-shape-protection/
description: This section explains how to remove shape protection using Aspose.Diagram for Python via Java.
---
## **Eliminar la protección de la forma Visio**
Protecting Visio shapes allow users to lock specific aspects of shapes. Aspects of shapes that can be locked through shape protection include width, height, x-position, y-position, rotation and more. Developers can achieve this using Aspose.Diagram for Python via Java.
### **Edite la protección de forma Visio**
**Bloquear aspecto**, **LockBegin**, **BloquearCalcWH**, **BloquearRecortar**, **LockCustProp**, **BloquearBorrar**, **LockEnd**, **formato de bloqueo**, **LockFromGroupFormat**, **Grupo de bloqueo**, **Altura de bloqueo**, **BloquearMoverX**, **LockMoveY**, **Bloquear Rotar**, **BloquearSeleccionar**, **BloquearTextoEditar**, **LockThemeColors**, **Efectos de tema de bloqueo**, **BloquearVtxEditar** y**ancho de bloqueo** propiedades expuestas por**Proteccion** apoyo de la clase**Aspose.Diagram.BoolValue** objeto. Estas propiedades se pueden utilizar para proteger y desproteger formas.

En Microsoft Office Visio, el usuario puede realizar las siguientes acciones para proteger cualquier forma:

- Abierto diagram en Microsoft Office Visio
- Seleccione cualquier forma
- Seleccione 'Protección' en el menú 'Formato' si está usando Visio 2007 o seleccione 'Protección' en el menú 'Desarrollador' si está usando Visio 2010
- En la ventana 'Protección', desmarque cualquier cuadro de texto para desbloquear cualquier atributo de forma
- Presiona OK'

### **Eliminar la muestra de programación de protección de forma**
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

