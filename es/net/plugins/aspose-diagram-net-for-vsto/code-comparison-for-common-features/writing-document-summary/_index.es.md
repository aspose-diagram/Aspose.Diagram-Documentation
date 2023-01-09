---
title: Resumen del documento de escritura
type: docs
weight: 70
url: /es/net/writing-document-summary/
---
## **VSTO**
A continuación se muestra el código para escribir el resumen del documento de Visio:

{{< highlight "cs" >}}

  Application.ActiveDocument.Creator = "Zeeshan";

 Application.ActiveDocument.Company = "Aspose";

 Application.ActiveDocument.Category = "Drawing 2D";

 Application.ActiveDocument.Manager = "Self";

 Application.ActiveDocument.Title = "Zeeshan";

 Application.ActiveDocument.Subject = "Visio Diagram";


{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

Microsoft Visio le permite definir una serie de propiedades de información de resumen del documento para ayudarlo a usted y a sus colegas a identificar un diagram. Las propiedades de resumen, por ejemplo, título, tema, autor y descripción, hacen que el archivo sea más fácil de encontrar al buscar y más fácil de reconocer al navegar archivos

{{% /alert %}} 
### **Escritura Microsoft Visio Resumen del documento Información**
 los[Propiedades del documento](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties)La clase expone una serie de propiedades para establecer u obtener información de resumen de Microsoft Visio diagram. Aspose.Diagram for .NET puede actualizar la información de resumen del dibujo y luego volver a escribir el archivo de dibujo en VDX.

Para actualizar la información de resumen del dibujo de un archivo VDX o VSD existente:

1.  Crear una instancia de la[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram) clase.
1. Establezca las propiedades expuestas por Diagram.DocumentProps para definir la información de resumen para el archivo de dibujo Visio.
1. Llame al método Guardar de la clase Diagram para escribir el archivo de dibujo Visio en VDX.

Consulta la información resumida:

1. Abra el archivo de salida VDX en Microsoft Visio.
1.  Seleccionando**Información** desde el**Expediente** menú.

{{< highlight "cs" >}}

  //Call the diagram constructor to load diagram from a VDX file

 Diagram vdxDiagram = new Diagram("Drawing1.vdx");

 //Set some summary information about the diagram

 vdxDiagram.DocumentProps.Creator = "Ijaz";

 vdxDiagram.DocumentProps.Company = "Aspose";

 vdxDiagram.DocumentProps.Category = "Drawing 2D";

 vdxDiagram.DocumentProps.Manager = "Sergey Polshkov";

 vdxDiagram.DocumentProps.Title = "Aspose Title";

 vdxDiagram.DocumentProps.TimeCreated = DateTime.Now;

 vdxDiagram.DocumentProps.Subject = "Visio Diagram";

 vdxDiagram.DocumentProps.Template = "Aspose Template";

 //Write the updated file to the disk in VDX file format

 vdxDiagram.Save("output.vdx", SaveFileFormat.VDX);


{{< /highlight >}}
## **Descargar código de muestra**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Descargar código de ejecución**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Writing%20Document%20Summary)
