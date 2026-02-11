---
title: Конвертировать форму Visio в PDF
type: docs
weight: 10
url: /ru/java/convert-a-visio-shape-to-pdf/
description: В этом разделе объясняется, как преобразовать форму visio в PDF с помощью Aspose.Diagram.
---
## ** Преобразование формы visio в PDF**
 Метод ToPdf, предоставляемый[Форма](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) класс можно использовать для преобразования в pdf.

В приведенном ниже коде показано, как:

1. Загрузите образец diagram.
1. получить конкретную страницу.
1. получить определенную форму.
1. преобразовать форму в pdf.
### **Форма в PDF**
Используйте следующий код в своем Java-приложении, чтобы преобразовать форму visio в PDF.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ShapeToPdf.class); 
// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToPdf.vsdx");

// Get a particular page
Page page = diagram.getPages().get(0);

// Get a particular shape
Shape shape = page.getShapes().get(0);

// Shape to Pdf
shape.toPdf("out.pdf");
{{< /highlight >}}
```


