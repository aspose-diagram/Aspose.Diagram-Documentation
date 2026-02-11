---
title: Преобразование формы Visio в изображение
type: docs
weight: 10
url: /ru/java/convert-a-visio-shape-to-image/
description: В этом разделе объясняется, как преобразовать фигуру visio в изображение с помощью Aspose.Diagram.
---
## **Преобразование фигуры visio в изображение**
 Метод ToImage, предоставляемый[Форма](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) класс можно использовать для преобразования в изображение.

В приведенном ниже коде показано, как:

1. Загрузите образец diagram.
1. получить конкретную страницу.
1. получить определенную форму.
1. преобразовать форму в изображение.
### **Форма для изображения**
Используйте следующий код в своем Java-приложении, чтобы преобразовать фигуру visio в изображение.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ShapeToImage.class); 
// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToImage.vsdx");

// Get a particular page
Page page = diagram.getPages().get(0);

// Get a particular shape
Shape shape = page.getShapes().get(0);

// Shape to image
com.aspose.diagram.ImageSaveOptions option = new com.aspose.diagram.ImageSaveOptions(SaveFileFormat.PNG);
shape.toImage("out.png",option);
{{< /highlight >}}



