---
title: Agregar punto de conexión a la forma
type: docs
weight: 70
url: /es/net/add-connection-point-to-shape/
description: Esta sección explica cómo agregar un punto de conexión a una forma visio con Aspose.Diagram.
---
## **Agregar punto de conexión a una forma en Visio**
Este tema explica cómo los desarrolladores pueden agregar un punto de conexión a una forma visio usando Aspose.Diagram for .NET.
### **Agregar punto de conexión**
 los[Conexiones](https://reference.aspose.com/diagram/net/aspose.diagram/shape/properties/connections) El objeto representa la colección de conexiones en el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) clase.

El siguiente código muestra cómo:

1. Cargue una muestra diagram.
1. obtener una página en particular.
1. obtener una forma particular.
1. nueva una conexión
1.  establecer la propiedad de conexión
1. agregar conexión a la forma
1. guardar diagram
#### **Agregar punto de conexión a la forma Ejemplo de programación**
Use el siguiente código en su aplicación .NET para agregar una conexión a una forma usando Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");

// Get a particular page
Page page = diagram.Pages.GetPage("Page-3");
// Get a dynamic connector type shape by id
Shape shape = page.Shapes.GetShape(18);
// Set dynamic connector appearance
shape.SetConnectorsType(ConnectorsTypeValue.StraightLines);

// Saving Visio diagram
diagram.Save(dataDir + "SetConnectorAppearance_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

