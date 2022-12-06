---
title: Público API Cambios en Aspose.Diagram 17.01
type: docs
weight: 10
url: /es/net/public-api-changes-in-aspose-diagram-17-01/
---
{{% alert color="primary" %}} 

Este documento describe los cambios al Aspose.Diagram API de la versión 16.12.0 a la 17.1.0, que pueden ser de interés para los desarrolladores de módulos/aplicaciones. Incluye no solo métodos públicos nuevos y actualizados, sino también una descripción de cualquier cambio en el comportamiento detrás de escena en Aspose.Diagram.

{{% /alert %}} 
## **Convert Visio Dibujo con formas selectivas**
Los desarrolladores pueden seleccionar formas específicas para convertir el dibujo Visio a cualquier otro formato compatible. hemos añadido[formas](http://www.aspose.com/api/net/diagram/aspose.diagram.saving/renderingsaveoptions/properties/shapes)miembro en el[RepresentaciónGuardarOpciones](http://www.aspose.com/api/net/diagram/aspose.diagram.saving/renderingsaveoptions)clase para este propósito. Cada clase de opción de guardado es la forma extendida de la clase RenderingSaveOptions. Por favor, compruebe el ejemplo de código:

**C#**

{{< highlight "csharp" >}}

 // the path to the documents directory.

string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// call the diagram constructor to load diagram from a VSD file

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance SVG save options class

SVGSaveOptions options = new SVGSaveOptions();

ShapeCollection shapes = options.Shapes;

// get shapes by page index and shape ID, and then add in the shape collection object

shapes.Add(diagram.Pages[0].Shapes.GetShape(1));

shapes.Add(diagram.Pages[0].Shapes.GetShape(2));

// save Visio drawing

diagram.Save(dataDir + "SelectiveShapes_out.svg", options);

{{< /highlight >}}
