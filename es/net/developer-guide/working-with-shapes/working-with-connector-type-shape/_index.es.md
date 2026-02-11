---
title: Trabajo con forma de tipo de conector
type: docs
weight: 70
url: /es/net/working-with-connector-type-shape/
description: Esta sección explica cómo configurar la apariencia del conector con Aspose.Diagram.
---
## **Establecer apariencia de la forma del tipo de conector en Visio**
Este tema explica cómo los desarrolladores pueden cambiar la apariencia de la forma del tipo de conector dinámico usando Aspose.Diagram for .NET.
### **Establecer la apariencia del conector**
 El método SetConnectorsType expuesto por el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La clase se puede utilizar para establecer la apariencia de la forma del tipo de conector.

El siguiente código muestra cómo:

1. Cargue una muestra diagram.
1. obtener una página en particular.
1. obtener una forma de conector particular.
1. establecer la apariencia de la forma.
1. guardar diagram
#### **Ejemplo de programación de la apariencia del conector establecido**
Use el siguiente código en su aplicación .NET para establecer la apariencia de la forma del tipo de conector usando Aspose.Diagram for .NET.


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

## **Seleccione la opción de redirección de la forma del conector**
 La propiedad ConFixedCode expuesta por el[Diseño](http://www.aspose.com/api/net/diagram/aspose.diagram/layout) La clase se puede utilizar para seleccionar la opción de redirección. La propiedad Layout, expuesta por el[Forma](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) clase, se utilizará.

El siguiente código muestra cómo:

1. Cargue un archivo de muestra.
1. obtener una página en particular.
1. obtener una forma de conector particular.
1. establecer opciones de redirección.
1. guardar diagram.
### **Seleccionar ejemplo de programación de opción de redirección**
Use el siguiente código en su aplicación .NET para seleccionar la opción de cambio de ruta de la forma del conector usando Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

// Get a particular connector shape
Shape shape = page.Shapes.GetShape(18);
// Set reroute option
shape.Layout.ConFixedCode.Value = ConFixedCodeValue.NeverReroute;

// Save Visio diagram
diagram.Save(dataDir + "RerouteConnectors_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

