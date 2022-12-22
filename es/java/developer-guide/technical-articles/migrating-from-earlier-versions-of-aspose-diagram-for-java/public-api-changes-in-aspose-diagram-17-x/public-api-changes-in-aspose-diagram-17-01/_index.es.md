---
title: Público API Cambios en Aspose.Diagram 17.01
type: docs
weight: 10
url: /es/java/public-api-changes-in-aspose-diagram-17-01/
---
{{% alert color="primary" %}} 

Este documento describe los cambios al Aspose.Diagram API de la versión 16.12.0 a la 17.01, que pueden ser de interés para los desarrolladores de módulos/aplicaciones. Incluye no solo métodos públicos nuevos y actualizados, sino también una descripción de cualquier cambio en el comportamiento detrás de escena en Aspose.Diagram.

{{% /alert %}} 
### **Convert Visio Dibujo con formas selectivas**
Los desarrolladores pueden seleccionar formas específicas para convertir el dibujo Visio a cualquier otro formato compatible. Hemos agregado el miembro Shapes en la clase RenderingSaveOptions para este propósito. Cada clase de opción de guardado es la forma extendida de la clase RenderingSaveOptions. Por favor, compruebe el ejemplo de código:

**Java**

{{< highlight "csharp" >}}

 // The path to the documents directory.

String dataDir = Utils.getSharedDataDir(ConvertVisioWithSelectiveShapes.class) + "LoadSaveConvert\\";

// call the diagram constructor to load diagram from a VSD file

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance SVG save options class

SVGSaveOptions options = new SVGSaveOptions();

ShapeCollection shapes = options.getShapes();

// get shapes by page index and shape ID, and then add in the shape collection object

shapes.add(diagram.getPages().get(0).getShapes().getShape(1));

shapes.add(diagram.getPages().get(0).getShapes().getShape(2));

// save Visio drawing

diagram.save(dataDir + "SelectiveShapes_out.svg", options);

{{< /highlight >}}
