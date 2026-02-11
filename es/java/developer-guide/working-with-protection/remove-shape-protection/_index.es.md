---
title: Eliminar protección de forma
type: docs
weight: 20
url: /es/java/remove-shape-protection/
description: Esta sección explica cómo quitar la protección de forma usando Aspose.Diagram.
---
## **Eliminar la protección de la forma Visio**
 La protección de formas Visio permite a los usuarios bloquear aspectos específicos de las formas. Los aspectos de las formas que se pueden bloquear a través de la protección de formas incluyen el ancho, la altura, la posición x, la posición y, la rotación y más. Los desarrolladores pueden lograr esto usando[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).
### **Edite la protección de forma Visio**
**Bloquear aspecto**, **LockBegin**, **BloquearCalcWH**, **BloquearRecortar**, **LockCustProp**, **BloquearBorrar**, **LockEnd**, **formato de bloqueo**, **LockFromGroupFormat**, **Grupo de bloqueo**, **Altura de bloqueo**, **BloquearMoverX**, **LockMoveY**, **Bloquear Rotar**, **BloquearSeleccionar**, **BloquearTextoEditar**, **LockThemeColors**, **Efectos de tema de bloqueo**, **BloquearVtxEditar** y**ancho de bloqueo** propiedades expuestas por[**Proteccion**](https://reference.aspose.com/diagram/java/com.aspose.diagram/protection) apoyo de la clase**Aspose.Diagram.BoolValue** objeto. Estas propiedades se pueden utilizar para proteger y desproteger formas.

En Microsoft Office Visio, el usuario puede realizar las siguientes acciones para proteger cualquier forma:

- Abierto diagram en Microsoft Office Visio
- Seleccione cualquier forma
- Seleccione 'Protección' en el menú 'Formato' si está usando Visio 2007 o seleccione 'Protección' en el menú 'Desarrollador' si está usando Visio 2010
- En la ventana 'Protección', desmarque cualquier cuadro de texto para desbloquear cualquier atributo de forma
- Presiona OK'
### **Eliminar la muestra de programación de protección de forma**
Use el siguiente código en su aplicación Java para hacer lo mismo (desbloquear cualquier atributo de forma) usando Aspose.Diagram for Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VisioShapeProtection.class);
//Load diagram
Diagram diagram = new Diagram(dataDir + "ProtectAndUnprotect.vsd");
// get page by name
Page page = diagram.getPages().getPage("Flow 1");
// get shape by ID
Shape shape = page.getShapes().getShape(1);

// set protections
shape.getProtection().getLockAspect().setValue(BOOL.FALSE);
shape.getProtection().getLockBegin().setValue(BOOL.FALSE);
shape.getProtection().getLockCalcWH().setValue(BOOL.FALSE);
shape.getProtection().getLockCrop().setValue(BOOL.FALSE);
shape.getProtection().getLockCustProp().setValue(BOOL.FALSE);
shape.getProtection().getLockDelete().setValue(BOOL.FALSE);
shape.getProtection().getLockEnd().setValue(BOOL.FALSE);
shape.getProtection().getLockFormat().setValue(BOOL.FALSE);
shape.getProtection().getLockFromGroupFormat().setValue(BOOL.FALSE);
shape.getProtection().getLockGroup().setValue(BOOL.FALSE);
shape.getProtection().getLockHeight().setValue(BOOL.FALSE);
shape.getProtection().getLockMoveX().setValue(BOOL.FALSE);
shape.getProtection().getLockMoveY().setValue(BOOL.FALSE);
shape.getProtection().getLockRotate().setValue(BOOL.FALSE);
shape.getProtection().getLockSelect().setValue(BOOL.FALSE);
shape.getProtection().getLockTextEdit().setValue(BOOL.FALSE);
shape.getProtection().getLockThemeColors().setValue(BOOL.FALSE);
shape.getProtection().getLockThemeEffects().setValue(BOOL.FALSE);
shape.getProtection().getLockVtxEdit().setValue(BOOL.FALSE);
shape.getProtection().getLockWidth().setValue(BOOL.FALSE);
        
// save diagram
diagram.save(dataDir + "VisioShapeProtection_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

