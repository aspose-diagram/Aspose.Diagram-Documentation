---
title: Настройка ячеек в разделе событий ShapeSheet
type: docs
weight: 10
url: /ru/java/setting-cells-in-the-event-section-of-shapesheet/
---
{{% alert color="primary" %}} 

Используя Aspose.Diagram API, разработчики могут определить, как фигура реагирует на определенные действия пользователя, написав Visio формулы, которые автоматически обрабатывают события. Всякий раз, когда пользователь выполняет одно из действий, описанных ниже, вычисляется формула в соответствующей ячейке таблицы свойств фигуры.

- **Текст** - Элемент события, который оценивается при изменении текста фигуры или текстовой композиции.
- **EventXFMod** - Положение, размер или ориентация фигуры на странице изменены.
- **СобытиеDblClick** - Форма дважды щелкнута.
- **СобытиеDrop** Новый экземпляр создается путем вставки, дублирования или перетаскивания фигуры или путем перетаскивания мастера.
- **СобытиеMultiDrop** - когда создается несколько новых экземпляров путем вставки, дублирования или перетаскивания фигуры или путем перетаскивания мастера.
- **Данные** - Зарезервировано для использования в будущем.

{{% /alert %}} 
## **Настройка ячеек событий**
[Мероприятие](https://reference.aspose.com/diagram/java/com.aspose.diagram/event) class позволяет разработчикам устанавливать ячейки событий в таблице свойств фигуры. В этом разделе справки показано, как разработчики могут устанавливать формулы в ячейках событий:

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
