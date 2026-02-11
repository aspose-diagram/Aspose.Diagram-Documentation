---
title: Извлечение элемента управления ActiveX из объекта Shape для изменения свойств
type: docs
weight: 20
url: /ru/net/retrieve-an-activex-control-from-a-shape-object-to-modify-properties/
description: Измените свойства элемента управления ActiveX с помощью библиотеки Aspose.Diagram.
---
{{% alert color="primary" %}} 

Используя Aspose.Diagram API, разработчики могут получить элемент управления ActiveX из объекта формы Visio, чтобы установить все его доступные свойства.

{{% /alert %}} 
## **Получение примера программирования элемента управления ActiveX**
[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Класс предлагает свойство ActiveXControl, которое позволяет разработчикам извлекать элемент управления ActiveX из объекта формы Visio. Разработчики могут преобразовать элемент управления ActiveX в соответствующий класс элемента управления ActiveX, а затем установить все его доступные свойства.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioActiveXControls();
// Load and get a Visio page by name
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");            
Page page = diagram.Pages.GetPage("Page-1");
// Get a shape by ID
Shape shape = page.Shapes.GetShape(1);
// Get an ActiveX control
CommandButtonActiveXControl cbac = (CommandButtonActiveXControl)shape.ActiveXControl;
// Set width, height and caption of the command button control
cbac.Width = 4;           
cbac.Height = 4;           
cbac.Caption = "Test Button";
// Save diagram
diagram.Save(dataDir + "RetrieveActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

