---
title: Добавить точку соединения к фигуре
type: docs
weight: 70
url: /ru/net/add-connection-point-to-shape/
description: В этом разделе объясняется, как добавить точку соединения в фигуру visio с помощью Aspose.Diagram.
---
## **Добавить точку соединения к фигуре в Visio**
В этом разделе подробно описывается, как разработчики могут добавить точку соединения к фигуре visio, используя Aspose.Diagram for .NET.
### **Добавить точку подключения**
[Соединения](https://reference.aspose.com/diagram/net/aspose.diagram/shape/properties/connections) объект представляет коллекцию соединений в[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) учебный класс.

В приведенном ниже коде показано, как:

1. Загрузите образец diagram.
1. получить конкретную страницу.
1. получить определенную форму.
1. новое соединение
1.  установить свойство подключения
1. добавить соединение в форму
1. сохранить diagram
#### **Добавить точку соединения в форму Образец программирования**
Используйте следующий код в своем приложении .NET, чтобы добавить подключение к фигуре с помощью Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");

// Get a particular page
Page page = diagram.Pages.GetPage("Page-3");
// Get a dynamic connector type shape by id
Shape shape = page.Shapes.GetShape(18);
// Set dynamic connector appearance
shape.SetConnectorsType(ConnectorsTypeValue.StraightLines);

// Saving Visio diagram
diagram.Save(dataDir + "SetConnectorAppearance_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

