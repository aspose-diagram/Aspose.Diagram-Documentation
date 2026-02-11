---
title: Configuración de celdas en la sección de eventos de ShapeSheet
type: docs
weight: 10
url: /es/java/setting-cells-in-the-event-section-of-shapesheet/
---
{{% alert color="primary" %}} 

Usando Aspose.Diagram API, los desarrolladores pueden definir cómo responde una forma a acciones específicas del usuario escribiendo Visio fórmulas que manejan eventos automáticamente. Cada vez que el usuario realiza una de las acciones descritas a continuación, se evalúa la fórmula en la celda ShapeSheet correspondiente.

- **El texto** - Un elemento de evento que se evalúa cuando cambia el texto de una forma o la composición del texto.
- **EventXFMod** - Se cambia la posición, el tamaño o la orientación de la forma en la página.
- **EventDblClick** - Se hace doble clic en la forma.
- **EventDrop** Se crea una nueva instancia pegando, duplicando o arrastrando una forma, o arrastrando y soltando un maestro.
- **EventoMultiDrop** - cuando se crean varias instancias nuevas al pegar, duplicar o arrastrar una forma, o al arrastrar y soltar un patrón.
- **Los datos** - Reservado para utilización futura.

{{% /alert %}} 
## **Configuración de celdas de eventos**
[Evento](https://reference.aspose.com/diagram/java/com.aspose.diagram/event) class permite a los desarrolladores establecer celdas de eventos en ShapeSheet. Este tema de ayuda demuestra cómo los desarrolladores pueden establecer fórmulas en las celdas de eventos:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SettingEventCells.class);
// load diagram
Diagram diagram = new Diagram(dataDir + "TestTemplate.vsdm");
// get page
Page page = diagram.getPages().get(0);
// get shape id
long shapeId = page.addShape(3.0, 3.0, 0.36, 0.36, "Square");
// get shape
Shape shape = page.getShapes().getShape(shapeId);

// set event cells in the ShapeSheet
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");
shape.getEvent().getEventXFMod().getUfe().setF("CALLTHIS(\"ThisDocument.ShowAlert\")");

// save diagram
diagram.save(dataDir + "Output_NET.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```
