---
title: Actualizar datos de formas
type: docs
weight: 40
url: /es/net/refresh-shapes-data/
description: Esta sección explica cómo actualizar los datos de la forma para una forma visio con Aspose.Diagram.
---
## **Actualiza la posición de la forma incluyendo xform, conexión y geom al cambiar el texto de la forma o de otra**
 El método RefreshData expuesto por el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) la clase se puede usar para actualizar los datos de la forma

El siguiente código muestra cómo:

1. Cargue un archivo de muestra.
1. Accede a una forma particular.
1. Actualizar los datos de la forma.
### **Actualizar los datos de Shape**
Use el siguiente código en su aplicación .NET para actualizar una forma usando Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

// Get Shape
Shape shape = page.Shapes.GetShape(15);

// Refresh data
shape.RefreshData();

// Save visio diagram
diagram.Save(dataDir + "RefreshData_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


