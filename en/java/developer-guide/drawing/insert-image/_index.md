---
title: Insert Image
type: docs
weight: 70
url: /java/drawing/insert-image
description: This section explains how to insert a image in a visio page with Aspose.Diagram. Support using java to insert image and save as pdf, svg, html, image, xps and other formats.
---
The [Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) object represents the drawing area of a foreground page or a background page. The Pages property exposed by the [Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class supports a collection of Aspose.Diagram.Page objects. 

## **Insert Image in Visio**
Aspose.Diagram for JAVA API allows developers to insert a image shape in a page. The code example below shows how to insert a image in a Visio drawing.


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


## **Insert Image in SVG**
Aspose.Diagram for JAVA API allows developers to insert a image shape in a page. The code example below shows how to insert a image in a Visio drawing and save as SVG format.


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


## **Insert Image in PNG**
Aspose.Diagram for JAVA API allows developers to insert a image shape in a page. The code example below shows how to insert a image in a Visio drawing and save as PNG format.


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


## **Insert Image in PDF**
Aspose.Diagram for JAVA API allows developers to insert a image shape in a page. The code example below shows how to insert a image in a Visio drawing and save as PDF format.


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


## **Insert Image in HTML**
Aspose.Diagram for JAVA API allows developers to insert a image shape in a page. The code example below shows how to insert a image in a Visio drawing and save as HTML format.


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

