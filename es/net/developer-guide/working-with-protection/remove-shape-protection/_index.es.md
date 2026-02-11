---
title: Eliminar protección de forma
type: docs
weight: 20
url: /es/net/remove-shape-protection/
description: En esta sección se explica cómo eliminar la protección de formas.
---
## **Eliminar la protección de la forma Visio**
 La protección de formas Visio permite a los usuarios bloquear aspectos específicos de las formas. Los aspectos de las formas que se pueden bloquear a través de la protección de formas incluyen el ancho, la altura, la posición x, la posición y, la rotación y más. Los desarrolladores pueden lograr esto usando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Edite la protección de forma Visio**
**Bloquear aspecto**, **LockBegin**, **BloquearCalcWH**, **BloquearRecortar**, **LockCustProp**, **BloquearBorrar**, **LockEnd**, **formato de bloqueo**, **LockFromGroupFormat**, **Grupo de bloqueo**, **Altura de bloqueo**, **BloquearMoverX**, **LockMoveY**, **Bloquear Rotar**, **BloquearSeleccionar**, **BloquearTextoEditar**, **LockThemeColors**, **Efectos de tema de bloqueo**, **BloquearVtxEditar** y**ancho de bloqueo** propiedades expuestas por[**Proteccion**](http://www.aspose.com/api/net/diagram/aspose.diagram/Protection) apoyo de la clase**Aspose.Diagram.BoolValue** objeto. Estas propiedades se pueden utilizar para proteger y desproteger formas.

En Microsoft Office Visio, el usuario puede realizar las siguientes acciones para proteger cualquier forma:

- Abierto diagram en Microsoft Office Visio
- Seleccione cualquier forma
- Seleccione 'Protección' en el menú 'Formato' si está usando Visio 2007 o seleccione 'Protección' en el menú 'Desarrollador' si está usando Visio 2010
- En la ventana 'Protección', desmarque cualquier cuadro de texto para desbloquear cualquier atributo de forma
- Presiona OK'
### **Eliminar la muestra de programación de protección de forma**
Use el siguiente código en su aplicación .NET para hacer lo mismo (desbloquear cualquier atributo de forma) usando Aspose.Diagram for .NET.

```
{{< highlight "csharp" >}}
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
shape.Protection.LockAspect.Value = BOOL.False;
shape.Protection.LockBegin.Value = BOOL.False;
shape.Protection.LockCalcWH.Value = BOOL.False;
shape.Protection.LockCrop.Value = BOOL.False;
shape.Protection.LockCustProp.Value = BOOL.False;
shape.Protection.LockDelete.Value = BOOL.False;
shape.Protection.LockEnd.Value = BOOL.False;
shape.Protection.LockFormat.Value = BOOL.False;
shape.Protection.LockFromGroupFormat.Value = BOOL.False;
shape.Protection.LockGroup.Value = BOOL.False;
shape.Protection.LockHeight.Value = BOOL.False;
shape.Protection.LockMoveX.Value = BOOL.False;
shape.Protection.LockMoveY.Value = BOOL.False;
shape.Protection.LockRotate.Value = BOOL.False;
shape.Protection.LockSelect.Value = BOOL.False;
shape.Protection.LockTextEdit.Value = BOOL.False;
shape.Protection.LockThemeColors.Value = BOOL.False;
shape.Protection.LockThemeEffects.Value = BOOL.False;
shape.Protection.LockVtxEdit.Value = BOOL.False;
shape.Protection.LockWidth.Value = BOOL.False;
            
// Save diagram
diagram.Save(dataDir + "RemoveShapeProtection_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
