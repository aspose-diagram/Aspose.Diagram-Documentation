---
title: Работа с формой типа соединителя
type: docs
weight: 70
url: /ru/net/working-with-connector-type-shape/
description: В этом разделе объясняется, как настроить внешний вид соединителя с помощью Aspose.Diagram.
---
## **Установите внешний вид формы типа соединителя в Visio**
В этом разделе подробно описывается, как разработчики могут изменить внешний вид формы типа динамического соединителя, используя Aspose.Diagram for .NET.
### **Установить внешний вид соединителя**
 Метод SetConnectorsType, предоставляемый[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class можно использовать для установки внешнего вида формы типа соединителя.

В приведенном ниже коде показано, как:

1. Загрузите образец diagram.
1. получить конкретную страницу.
1. получить конкретную форму разъема.
1. задать внешний вид формы.
1. сохранить diagram
#### **Пример программирования внешнего вида коннектора**
Используйте следующий код в своем приложении .NET, чтобы настроить внешний вид формы типа соединителя, используя Aspose.Diagram for .NET.


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

## **Выберите вариант перенаправления формы соединителя**
 Свойство ConFixedCode, предоставляемое[Макет](http://www.aspose.com/api/net/diagram/aspose.diagram/layout) класс можно использовать для выбора варианта перенаправления. Свойство Layout, предоставляемое[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) класс, будет использоваться.

В приведенном ниже коде показано, как:

1. Загрузите образец файла.
1. получить конкретную страницу.
1. получить конкретную форму разъема.
1. установить параметры перенаправления.
1. сохранить diagram.
### **Пример программирования выбора варианта перенаправления**
Используйте следующий код в своем приложении .NET, чтобы выбрать параметр повторной маршрутизации формы соединителя, используя Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

// Get a particular connector shape
Shape shape = page.Shapes.GetShape(18);
// Set reroute option
shape.Layout.ConFixedCode.Value = ConFixedCodeValue.NeverReroute;

// Save Visio diagram
diagram.Save(dataDir + "RerouteConnectors_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

