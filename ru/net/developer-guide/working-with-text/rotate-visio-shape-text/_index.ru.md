---
title: Повернуть Visio Форма текста
type: docs
weight: 9
url: /ru/net/rotate-visio-shape-text/
keywords: Rotate, visio, Tex
description: Как повернуть текст формы в visio, используя .NET Diagram API.
---
## **Создание Diagram**
 Aspose.Diagram for .NET позволяет читать и создавать Microsoft Visio диаграммы из ваших собственных приложений без автоматизации. Первым шагом при создании новых документов является создание diagram. Затем[добавить фигуры и соединители](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)для создания diagram. Используйте конструктор по умолчанию[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) класс для создания нового diagram.
### **Образец программирования**
```
{{< highlight "csharp" >}}
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
```

Этот пример работает следующим образом:

1. Создайте объект класса Diagram.
1. Получить конкретную страницу
1. Получить патикулярную форму
1. Получить текст формы и повернуть текст
1. Вызовите метод Save объекта класса Diagram, а также передайте полный путь к файлу и объект DiagramSaveOptions.
### **Пример программирования поворота текста**
В следующем примере кода показано, как повернуть текст в файле Visio diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "UpdateShapeText.vsd");
// Get page by name
Page page = diagram.Pages.GetPage("Flow 1");
// Find a particular shape and update its text
foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.NameU.ToLower() == "process" && shape.ID == 1)
    {
        shape.Text.Value.Clear();
        shape.Text.Value.Add(new Txt("New Text"));
        // Set orientation angle
        double angleDeg = 90;
        double angleRad = (Math.PI / 180) * angleDeg;
        shape.TextXForm.TxtAngle.Value = angleRad;
    }
}
// Save diagram
diagram.Save(dataDir + "UpdateShapeText_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
