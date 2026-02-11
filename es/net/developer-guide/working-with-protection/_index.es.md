---
title: Trabajando con Protección
type: docs
weight: 170
url: /es/net/working-with-protection/
description: Esta sección explica cómo configurar la protección en el diagram con Aspose.Diagram.
---
## **Establecer Protección del Visio Diagram**
 La protección de diagramas permite a los usuarios bloquear fondos, patrones (plantillas), formas y estilos para que no se puedan editar. Esto es útil para proteger los estilos corporativos, por ejemplo, y garantizar una apariencia coherente en un conjunto de diagramas. Los desarrolladores pueden lograr esto usando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Edite la protección Visio Diagram**
Las propiedades ProtectBkgnds, ProtectMasters, ProtectShapes y ProtectStyles, expuestas por el[Configuración del documento](http://www.aspose.com/api/net/diagram/aspose.diagram/documentsettings) La clase admite el objeto Aspose.Diagram.BoolValue. Estas propiedades se pueden utilizar para proteger y desproteger diagramas Microsoft Office Visio. En el Microsoft Visio proteges los documentos de esta manera:

1. Abra un diagram en Microsoft Visio.
1. Abra la ventana Explorador de dibujos.
1.  Haga clic derecho en diagram y seleccione**Proteger documento** del menú.
1. En la ventana Proteger documento, marque o borre las opciones para bloquear o desbloquear diferentes elementos diagram.
1.  Hacer clic**OK**.
#### **Edite la muestra de programación de protección Diagram**
Use el código a continuación en una aplicación .NET para realizar las mismas tareas, como bloquear y desbloquear diferentes elementos del Visio diagram usando Aspose.Diagram for .NET API.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Protection();

// Load diagram
Diagram diagram = new Diagram(dataDir + "ProtectAndUnprotect.vsd");

diagram.DocumentSettings.ProtectBkgnds = BOOL.True;
diagram.DocumentSettings.ProtectMasters = BOOL.True;
diagram.DocumentSettings.ProtectShapes = BOOL.True;
diagram.DocumentSettings.ProtectStyles = BOOL.True;
// Save diagram
diagram.Save(dataDir + "VisioDiagramProtection_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

## **Establecer protección de la forma Visio**
 La protección de formas Visio permite a los usuarios bloquear aspectos específicos de las formas. Los aspectos de las formas que se pueden bloquear a través de la protección de formas incluyen el ancho, la altura, la posición x, la posición y, la rotación y más. Los desarrolladores pueden lograr esto usando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Edite la protección de forma Visio**
**Bloquear aspecto**, **LockBegin**, **BloquearCalcWH**, **BloquearRecortar**, **LockCustProp**, **BloquearBorrar**, **LockEnd**, **formato de bloqueo**, **LockFromGroupFormat**, **Grupo de bloqueo**, **Altura de bloqueo**, **BloquearMoverX**, **LockMoveY**, **Bloquear Rotar**, **BloquearSeleccionar**, **BloquearTextoEditar**, **LockThemeColors**, **Efectos de tema de bloqueo**, **BloquearVtxEditar** y**ancho de bloqueo** propiedades expuestas por[**Proteccion**](http://www.aspose.com/api/net/diagram/aspose.diagram/Protection) apoyo de la clase**Aspose.Diagram.BoolValue** objeto. Estas propiedades se pueden utilizar para proteger y desproteger formas.

En Microsoft Office Visio, el usuario puede realizar las siguientes acciones para proteger cualquier forma:

- Abierto diagram en Microsoft Office Visio
- Seleccione cualquier forma
- Seleccione 'Protección...' en el menú 'Formato' si está usando Visio 2007 o seleccione 'Protección' en el menú 'Desarrollador' si está usando Visio 2010
- En la ventana 'Protección', marque/desmarque cualquier cuadro de texto para bloquear o desbloquear cualquier atributo de forma
- Presiona OK'
### **Edite el ejemplo de programación de protección de forma**
Use el siguiente código en su aplicación .NET para hacer lo mismo (bloquear/desbloquear cualquier atributo de forma) usando Aspose.Diagram for .NET.


{{< highlight csharp >}}
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
shape.Protection.LockAspect.Value = BOOL.True;
shape.Protection.LockBegin.Value = BOOL.True;
shape.Protection.LockCalcWH.Value = BOOL.True;
shape.Protection.LockCrop.Value = BOOL.True;
shape.Protection.LockCustProp.Value = BOOL.True;
shape.Protection.LockDelete.Value = BOOL.True;
shape.Protection.LockEnd.Value = BOOL.True;
shape.Protection.LockFormat.Value = BOOL.True;
shape.Protection.LockFromGroupFormat.Value = BOOL.True;
shape.Protection.LockGroup.Value = BOOL.True;
shape.Protection.LockHeight.Value = BOOL.True;
shape.Protection.LockMoveX.Value = BOOL.True;
shape.Protection.LockMoveY.Value = BOOL.True;
shape.Protection.LockRotate.Value = BOOL.True;
shape.Protection.LockSelect.Value = BOOL.True;
shape.Protection.LockTextEdit.Value = BOOL.True;
shape.Protection.LockThemeColors.Value = BOOL.True;
shape.Protection.LockThemeEffects.Value = BOOL.True;
shape.Protection.LockVtxEdit.Value = BOOL.True;
shape.Protection.LockWidth.Value = BOOL.True;
            
// Save diagram
diagram.Save(dataDir + "VisioShapeProtection_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

