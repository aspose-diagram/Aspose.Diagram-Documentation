---
title: Rotar Visio Texto de forma
type: docs
weight: 9
url: /es/net/rotate-visio-shape-text/
keywords: Rotate, visio, Tex
description: Cómo rotar el texto de la forma en visio usando .NET Diagram API.
---
## **Creando un Diagram**
 Aspose.Diagram for .NET le permite leer y crear diagramas Microsoft Visio desde sus propias aplicaciones, sin Microsoft Office automatización. El primer paso al crear nuevos documentos es crear un diagram. Luego[añadir formas y conectores](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)para construir el diagram. Use el constructor predeterminado de[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) clase para crear un nuevo diagram.
### **Ejemplo de programación**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Create directory if it is not already present.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Initialize a new Visio
Diagram diagram = new Diagram();
dataDir = dataDir + "CreateDiagram_out.vsdx";
// Save in the VSDX format
diagram.Save(dataDir, SaveFileFormat.VSDX);

{{< /highlight >}}
```

Este ejemplo funciona de la siguiente manera:

1. Cree un objeto de la clase Diagram.
1. Obtener página particular
1. Consigue una forma particular
1. Obtenga texto de forma y gire el texto
1. Llame al método Save del objeto de clase Diagram y también pase la ruta completa del archivo y el objeto DiagramSaveOptions.
### **Ejemplo de programación de rotar texto**
El siguiente código de ejemplo muestra cómo rotar texto en Visio diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "UpdateShapeText.vsd");
// Get page by name
Page page = diagram.Pages.GetPage("Flow 1");
// Find a particular shape and update its text
foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.NameU.ToLower() == "process" && shape.ID == 1)
    {
        shape.Text.Value.Clear();
        shape.Text.Value.Add(new Txt("New Text"));
        // Set orientation angle
        double angleDeg = 90;
        double angleRad = (Math.PI / 180) * angleDeg;
        shape.TextXForm.TxtAngle.Value = angleRad;
    }
}
// Save diagram
diagram.Save(dataDir + "UpdateShapeText_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
