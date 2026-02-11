---
title: Преобразование формы Visio в изображение
type: docs
weight: 10
url: /ru/net/convert-a-visio-shape-to-image/
description: В этом разделе объясняется, как преобразовать фигуру visio в изображение с помощью Aspose.Diagram.
---
## **Преобразование фигуры visio в изображение**
В этом разделе подробно описывается, как разработчики могут преобразовать фигуру visio в изображение с помощью Aspose.Diagram.
 Метод ToImage, предоставляемый[Форма](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) класс можно использовать для преобразования в изображение.


В приведенном ниже коде показано, как:

1. Загрузите образец diagram.
1. получить конкретную страницу.
1. получить определенную форму.
1. преобразовать форму в изображение.
#### **Образец программирования формы для изображения**
Используйте следующий код в своем приложении .net, чтобы преобразовать фигуру visio в изображение.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToImage.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

// Shape to Image
Aspose.Diagram.Saving.ImageSaveOptions o = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);
shape.ToImage("out.png", o);

{{< /highlight >}}

