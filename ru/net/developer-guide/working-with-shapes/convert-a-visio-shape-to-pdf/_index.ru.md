---
title: Конвертировать форму Visio в PDF
type: docs
weight: 10
url: /ru/net/convert-a-visio-shape-to-pdf/
description: В этом разделе объясняется, как преобразовать форму visio в PDF с помощью Aspose.Diagram.
---
## ** Преобразование формы visio в PDF**
 Метод ToPdf, предоставляемый[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) класс можно использовать для преобразования в pdf.

В приведенном ниже коде показано, как:

1. Загрузите образец diagram.
1. получить конкретную страницу.
1. получить определенную форму.
1. преобразовать форму в pdf.
### **Форма в PDF**
Используйте следующий код в своем приложении .net, чтобы преобразовать фигуру visio в PDF.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToPdf.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

// Shape to Pdf
shape.ToPdf("out.pdf");

{{< /highlight >}}
```

