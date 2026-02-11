---
title: Преобразование формы Visio в HTML
type: docs
weight: 10
url: /ru/java/convert-a-visio-shape-to-html/
description: В этом разделе объясняется, как преобразовать форму visio в HTML с помощью Aspose.Diagram.
---
## ** Преобразование формы visio в HTML**
 Метод ToHTML, предоставляемый[Форма](http://www.aspose.com/api/java/diagram/com.aspose.diagram/shape) класс можно использовать для преобразования в html.

В приведенном ниже коде показано, как:

1. Загрузите образец diagram.
1. получить конкретную страницу.
1. получить определенную форму.
1. преобразовать форму в html.
### **Форма в HTML**
Используйте следующий код в своем Java-приложении, чтобы преобразовать форму visio в HTML.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ShapeToHtml.class); 
// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToHtml.vsdx");

// Get a particular page
Page page = diagram.getPages().get(0);

// Get a particular shape
Shape shape = page.getShapes().get(0);

// Shape to HTML
HTMLSaveOptions hs = new HTMLSaveOptions();
shape.toHTML("out.htm", hs);
{{< /highlight >}}



