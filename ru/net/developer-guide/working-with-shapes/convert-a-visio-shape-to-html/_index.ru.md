---
title: Преобразование формы Visio в HTML
type: docs
weight: 10
url: /ru/net/convert-a-visio-shape-to-html/
description: В этом разделе объясняется, как преобразовать форму visio в HTML с помощью Aspose.Diagram.
---
## ** Преобразование формы visio в HTML**
 Метод ToHTML, предоставляемый[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) класс можно использовать для преобразования в html.

В приведенном ниже коде показано, как:

1. Загрузите образец diagram.
1. получить конкретную страницу.
1. получить определенную форму.
1. преобразовать форму в html.
### **Форма в HTML**
Используйте следующий код в своем приложении .net, чтобы преобразовать форму visio в HTML.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToHtml.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

// Shape to HTML
Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();
shape.ToHTML("out.htm", hs);

{{< /highlight >}}


