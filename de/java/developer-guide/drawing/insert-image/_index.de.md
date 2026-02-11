---
title: Bild einfügen
type: docs
weight: 70
url: /de/java/drawing/insert-image
description: In diesem Abschnitt wird erläutert, wie Sie ein Bild in eine visio-Seite mit Aspose.Diagram einfügen. Unterstützung der Verwendung von Java zum Einfügen von Bildern und zum Speichern als PDF, SVG, HTML, Bild, XPS und andere Formate.
---
 Das[Buchseite](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)Objekt stellt den Zeichenbereich einer Vordergrundseite oder einer Hintergrundseite dar. Die Pages-Eigenschaft, die von der[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) -Klasse unterstützt eine Sammlung von Aspose.Diagram.Page-Objekten.

## **Bild in Visio einfügen**
Aspose.Diagram für JAVA API ermöglicht Entwicklern das Einfügen einer Bildform in eine Seite. Das folgende Codebeispiel zeigt, wie Sie ein Bild in eine Visio-Zeichnung einfügen.

```
{{< highlight "java" >}}
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
```

## **Bild in SVG einfügen**
Aspose.Diagram for JAVA API allows developers to insert a image shape in a page. The code example below shows how to insert a image in a Visio drawing and save as SVG format.

```
{{< highlight "java" >}}
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
```

## **Bild in PNG einfügen**
Aspose.Diagram for JAVA API allows developers to insert a image shape in a page. The code example below shows how to insert a image in a Visio drawing and save as PNG format.

```
{{< highlight "java" >}}
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
```

## **Bild in PDF einfügen**
Aspose.Diagram for JAVA API allows developers to insert a image shape in a page. The code example below shows how to insert a image in a Visio drawing and save as PDF format.

```
{{< highlight "java" >}}
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
```

## **Bild in HTML einfügen**
Aspose.Diagram for JAVA API allows developers to insert a image shape in a page. The code example below shows how to insert a image in a Visio drawing and save as HTML format.

```
{{< highlight "java" >}}
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
```
