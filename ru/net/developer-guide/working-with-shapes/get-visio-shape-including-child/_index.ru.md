---
title: Получить форму Visio, включая дочернюю
type: docs
weight: 110
url: /ru/net/get-visio-shape-including-child/
description: В этом разделе объясняется, как получить фигуру visio, включая дочернюю фигуру с идентификатором или именем фигуры с Aspose.Diagram.
---
### **Получить форму Visio, включая дочернюю**
Каждая фигура в diagram имеет идентификатор и имя. Идентификатор важен при программировании с помощью Visio: это основной метод доступа к фигуре. Каждая фигура также сохраняет информацию о том, из какого шаблона (трафарета) она сделана.

 А[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) является объектом на рисунке Visio, у которого, возможно, есть отец или сыновья. Свойство Shapes, предоставляемое классом Page, поддерживает коллекцию объектов Aspose.Diagram.Shape. Свойство Shapes можно использовать для получения информации о фигуре.
#### **Получить Visio Образец программирования формы**
Следующий фрагмент кода извлекает фигуру, включая дочерний элемент. Пожалуйста, проверьте этот пример кода:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "NetworkConnection.vsdx");

Page page = diagram.Pages[0];

Shape shapeContainerChild = page.Shapes.GetShapeIncludingChild("RectangleChild");

if (shapeContainerChild == null)
    throw new Exception();
    
// Save visio diagram
diagram.Save(dataDir + "GroupShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


