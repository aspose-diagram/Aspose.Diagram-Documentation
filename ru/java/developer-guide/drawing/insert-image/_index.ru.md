---
title: Вставить изображение
type: docs
weight: 70
url: /ru/java/drawing/insert-image
description: В этом разделе объясняется, как вставить изображение на страницу visio с помощью Aspose.Diagram. Поддержка использования Java для вставки изображения и сохранения в форматах pdf, svg, html, image, xps и других форматах.
---
[Страница](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)объект представляет область рисования страницы переднего плана или страницы фона. Свойство Pages, предоставляемое[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) Класс поддерживает набор объектов Aspose.Diagram.Page.

## **Вставить изображение в Visio**
Aspose.Diagram для JAVA API позволяет разработчикам вставлять форму изображения на страницу. В приведенном ниже примере кода показано, как вставить изображение в чертеж Visio.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(AddImageToPage.class) + "Pages/";

// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Page-1");
double pinX = 3, pinY = 3, width = 4, hieght = 4;
File file = new File("image.png"); 
FileInputStream fis = new FileInputStream(file); 
page.addShape(pinX, pinY, width, hieght, fis);

// Save the Visio diagram
diagram.save(dataDir + "AddImageToPage_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


## **Вставить изображение в SVG**
Aspose.Diagram для JAVA API позволяет разработчикам вставлять форму изображения на страницу. В приведенном ниже примере кода показано, как вставить изображение в чертеж Visio и сохранить в формате SVG.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(AddImageToPage.class) + "Pages/";

// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Page-1");
double pinX = 3, pinY = 3, width = 4, hieght = 4;
File file = new File("image.png"); 
FileInputStream fis = new FileInputStream(file); 
page.addShape(pinX, pinY, width, hieght, fis);

// Save the Visio diagram
diagram.save(dataDir + "AddImageToPage_Out.svg", SaveFileFormat.SVG);

{{< /highlight >}}


## **Вставить изображение в PNG**
Aspose.Diagram для JAVA API позволяет разработчикам вставлять форму изображения на страницу. В приведенном ниже примере кода показано, как вставить изображение в чертеж Visio и сохранить в формате PNG.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(AddImageToPage.class) + "Pages/";

// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Page-1");
double pinX = 3, pinY = 3, width = 4, hieght = 4;
File file = new File("image.png"); 
FileInputStream fis = new FileInputStream(file); 
page.addShape(pinX, pinY, width, hieght, fis);

// Save the Visio diagram
diagram.save(dataDir + "AddImageToPage_Out.png", SaveFileFormat.PNG);

{{< /highlight >}}


## **Вставить изображение в PDF**
Aspose.Diagram для JAVA API позволяет разработчикам вставлять форму изображения на страницу. В приведенном ниже примере кода показано, как вставить изображение в чертеж Visio и сохранить в формате PDF.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(AddImageToPage.class) + "Pages/";

// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Page-1");
double pinX = 3, pinY = 3, width = 4, hieght = 4;
File file = new File("image.png"); 
FileInputStream fis = new FileInputStream(file); 
page.addShape(pinX, pinY, width, hieght, fis);

// Save the Visio diagram
diagram.save(dataDir + "AddImageToPage_Out.pdf", SaveFileFormat.PDF);

{{< /highlight >}}


## **Вставить изображение в HTML**
Aspose.Diagram для JAVA API позволяет разработчикам вставлять форму изображения на страницу. В приведенном ниже примере кода показано, как вставить изображение в чертеж Visio и сохранить в формате HTML.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(AddImageToPage.class) + "Pages/";

// load an existing Visio
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a particular page
Page page = diagram.getPages().getPage("Page-1");
double pinX = 3, pinY = 3, width = 4, hieght = 4;
File file = new File("image.png"); 
FileInputStream fis = new FileInputStream(file); 
page.addShape(pinX, pinY, width, hieght, fis);
// initialize PDF save options
HTMLSaveOptions options = new HTMLSaveOptions();
// Save the Visio diagram
diagram.save(dataDir + "ExportOfHiddenVisioPagesToHTML_Out.html", options);

{{< /highlight >}}

