---
title: Agregar marca de agua a Visio
type: docs
weight: 10
url: /es/net/add-watermark-to-visio/
keywords: watermark, visi
description: Cómo agregar una marca de agua a visio usando .NET Diagram API.
---
## **Creando un Diagram**
 Aspose.Diagram for .NET le permite leer y crear diagramas Microsoft Visio desde sus propias aplicaciones, sin Microsoft Office automatización. El primer paso al crear nuevos documentos es crear un diagram. Luego[añadir formas y conectores](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)para construir el diagram. Use el constructor predeterminado de[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) clase para crear un nuevo diagram.
### **Ejemplo de programación**

{{< highlight csharp >}}
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


Este ejemplo funciona de la siguiente manera:

1. Cree un objeto de la clase Diagram.
1. Agregar marca de agua a visio en la página
1. Llame al método Save del objeto de clase Diagram y también pase la ruta completa del archivo y el objeto DiagramSaveOptions.
### **Agregar marca de agua Ejemplo de programación**
El siguiente código de ejemplo muestra cómo agregar una marca de agua en Visio diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
static string text = "";
public static void Run()
{
    // The path to the documents directory.
    string dataDir = RunExamples.GetDataDir_ShapeText();
    // Load diagram
    Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");

    // Get Visio diagram page
    Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

    double pinx = page.PageSheet.PageProps.PageWidth.Value / 2;
    double piny = page.PageSheet.PageProps.PageHeight.Value / 2;
    double width = page.PageSheet.PageProps.PageWidth.Value;
    double height = page.PageSheet.PageProps.PageHeight.Value;
    
    //Add watermark
    Shape shape = page.AddText(pinx, piny, width, height, "Test text","Calibri","#a5a5a5",0.25);
    diagram.Save(dataDir + "Watermark.vsdx", SaveFileFormat.VSDX);
}


{{< /highlight >}}

