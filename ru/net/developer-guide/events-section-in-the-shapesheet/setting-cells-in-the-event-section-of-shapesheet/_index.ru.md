---
title: Настройка ячеек в разделе событий ShapeSheet
type: docs
weight: 10
url: /ru/net/setting-cells-in-the-event-section-of-shapesheet/
description: Управление свойствами событий файлов visio.
---
{{% alert color="primary" %}} 

Используя Aspose.Diagram API, разработчики могут определить, как фигура реагирует на определенные действия пользователя, написав Visio формулы, которые автоматически обрабатывают события. Всякий раз, когда пользователь выполняет одно из четырех действий, описанных ниже, вычисляется формула в соответствующей ячейке таблицы свойств фигуры.

- **Текст** - Элемент события, который оценивается при изменении текста фигуры или текстовой композиции.
- **EventXFMod** - Положение, размер или ориентация фигуры на странице изменены.
- **СобытиеDblClick** - Форма дважды щелкнута.
- **СобытиеDrop** Новый экземпляр создается путем вставки, дублирования или перетаскивания фигуры или путем перетаскивания мастера.
- **СобытиеMultiDrop** - когда создается несколько новых экземпляров путем вставки, дублирования или перетаскивания фигуры или путем перетаскивания мастера.
- **Данные** - Зарезервировано для использования в будущем.

{{% /alert %}} 
## **Настройка ячеек событий**
[Мероприятие](https://reference.aspose.com/diagram/net/aspose.diagram/event) class позволяет разработчикам устанавливать ячейки событий в таблице свойств фигуры. В этом разделе справки показано, как разработчики могут устанавливать формулы в ячейках событий:


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

