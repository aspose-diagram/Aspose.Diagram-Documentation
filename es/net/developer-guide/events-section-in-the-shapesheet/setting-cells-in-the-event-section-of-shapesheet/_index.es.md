---
title: Configuración de celdas en la sección de eventos de ShapeSheet
type: docs
weight: 10
url: /es/net/setting-cells-in-the-event-section-of-shapesheet/
description: Administre las propiedades de eventos de los archivos visio.
---
{{% alert color="primary" %}} 

Usando Aspose.Diagram API, los desarrolladores pueden definir cómo responde una forma a acciones específicas del usuario escribiendo Visio fórmulas que manejan eventos automáticamente. Cada vez que el usuario realiza una de las cuatro acciones descritas a continuación, se evalúa la fórmula en la celda ShapeSheet correspondiente.

- **El texto** - Un elemento de evento que se evalúa cuando cambia el texto de una forma o la composición del texto.
- **EventXFMod** - Se cambia la posición, el tamaño o la orientación de la forma en la página.
- **EventDblClick** - Se hace doble clic en la forma.
- **EventDrop** Se crea una nueva instancia pegando, duplicando o arrastrando una forma, o arrastrando y soltando un maestro.
- **EventoMultiDrop** - cuando se crean varias instancias nuevas al pegar, duplicar o arrastrar una forma, o al arrastrar y soltar un patrón.
- **Los datos** - Reservado para utilización futura.

{{% /alert %}} 
## **Configuración de celdas de eventos**
[Evento](https://reference.aspose.com/diagram/net/aspose.diagram/event) class permite a los desarrolladores establecer celdas de eventos en ShapeSheet. Este tema de ayuda demuestra cómo los desarrolladores pueden establecer fórmulas en las celdas de eventos:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_EventSection();

// Load diagram
Diagram diagram = new Diagram(dataDir + "TestTemplate.vsdm");
// Get page
Aspose.Diagram.Page page = diagram.Pages.GetPage(0);
// Get shape id
long shapeId = page.AddShape(3.0, 3.0, 0.36, 0.36, "Square");
// Get shape
Aspose.Diagram.Shape shape = page.Shapes.GetShape(shapeId);

// Set event cells in the ShapeSheet
shape.Event.EventXFMod.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.EventDblClick.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.EventDrop.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.EventMultiDrop.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.TheText.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";
shape.Event.TheData.Ufe.F = "CALLTHIS(\"ThisDocument.ShowAlert\")";

// Save diagram
diagram.Save(dataDir + "SettingCellsInEventSection_out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}

