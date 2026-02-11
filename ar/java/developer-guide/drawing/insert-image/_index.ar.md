---
title: إدراج صورة
type: docs
weight: 70
url: /ar/java/drawing/insert-image
description: يشرح هذا القسم كيفية إدراج صورة في صفحة visio مع Aspose.Diagram. دعم استخدام جافا لإدراج الصورة وحفظها بتنسيق pdf و svg و html و image و xps وتنسيقات أخرى.
---
 ال[صفحة](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)يمثل الكائن منطقة الرسم لصفحة أمامية أو صفحة خلفية. خاصية الصفحات التي يعرضها ملف[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) فئة تدعم مجموعة من Aspose.Diagram.Page كائنات.

## **أدخل الصورة في Visio**
Aspose.Diagram لـ JAVA API يسمح للمطورين بإدراج شكل صورة في الصفحة. يوضح مثال الكود أدناه كيفية إدراج صورة في رسم Visio.


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


## **أدخل الصورة في SVG**
Aspose.Diagram لـ JAVA API يسمح للمطورين بإدراج شكل صورة في الصفحة. يوضح مثال الكود أدناه كيفية إدراج صورة في رسم Visio وحفظها بتنسيق SVG.


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


## **أدخل الصورة في PNG**
Aspose.Diagram لـ JAVA API يسمح للمطورين بإدراج شكل صورة في الصفحة. يوضح مثال الكود أدناه كيفية إدراج صورة في رسم Visio وحفظها بتنسيق PNG.


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


## **أدخل الصورة في PDF**
Aspose.Diagram لـ JAVA API يسمح للمطورين بإدراج شكل صورة في الصفحة. يوضح مثال الكود أدناه كيفية إدراج صورة في رسم Visio وحفظها بتنسيق PDF.


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


## **أدخل الصورة في HTML**
Aspose.Diagram لـ JAVA API يسمح للمطورين بإدراج شكل صورة في الصفحة. يوضح مثال الكود أدناه كيفية إدراج صورة في رسم Visio وحفظها بتنسيق HTML.


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

