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

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-eventsection-SettingEventCells-SettingEventCells.java" >}}
