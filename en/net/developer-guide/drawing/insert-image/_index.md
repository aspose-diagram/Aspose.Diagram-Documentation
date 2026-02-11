---
title: Insert Image
type: docs
weight: 70
url: /net/drawing/insert-image
description: This section explains how to insert a image in a visio page with Aspose.Diagram. Support using C# to insert image and save as pdf, svg, html, image, xps and other formats.
---
The [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) object represents the drawing area of a foreground page or a background page. The Pages property exposed by the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class supports a collection of Aspose.Diagram.Page objects. 

## **Insert Image in Visio**
Aspose.Diagram for .NET API allows developers to insert a image shape in a page. The code example below shows how to insert a image in a Visio drawing.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page page = diagram.Pages[0];       
double pinX = 3, pinY = 3, width = 4, hieght = 4;
using (FileStream fs = new FileStream("image.png", FileMode.Open))
{
    page.AddShape(pinX, pinY, width, hieght, fs);
}
// Save diagram
diagram.Save(dataDir + "AddImageToPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


## **Insert Image in SVG**
Aspose.Diagram for .NET API allows developers to insert a image shape in a page. The code example below shows how to insert a image in a Visio drawing and save as SVG format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page page = diagram.Pages[0];       
double pinX = 3, pinY = 3, width = 4, hieght = 4;
using (FileStream fs = new FileStream("image.png", FileMode.Open))
{
    page.AddShape(pinX, pinY, width, hieght, fs);
}
// Save diagram
diagram.Save(dataDir + "AddImageToPage_out.svg", SaveFileFormat.SVG);

{{< /highlight >}}


## **Insert Image in PNG**
Aspose.Diagram for .NET API allows developers to insert a image shape in a page. The code example below shows how to insert a image in a Visio drawing and save as PNG format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page page = diagram.Pages[0];       
double pinX = 3, pinY = 3, width = 4, hieght = 4;
using (FileStream fs = new FileStream("image.png", FileMode.Open))
{
    page.AddShape(pinX, pinY, width, hieght, fs);
}
// Save diagram
diagram.Save(dataDir + "AddImageToPage_out.png", SaveFileFormat.PNG);

{{< /highlight >}}


## **Insert Image in PDF**
Aspose.Diagram for .NET API allows developers to insert a image shape in a page. The code example below shows how to insert a image in a Visio drawing and save as PDF format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page page = diagram.Pages[0];       
double pinX = 3, pinY = 3, width = 4, hieght = 4;
using (FileStream fs = new FileStream("image.png", FileMode.Open))
{
    page.AddShape(pinX, pinY, width, hieght, fs);
}
// Save diagram
diagram.Save(dataDir + "AddImageToPage_out.pdf", SaveFileFormat.PDF);

{{< /highlight >}}


## **Insert Image in HTML**
Aspose.Diagram for .NET API allows developers to insert a image shape in a page. The code example below shows how to insert a image in a Visio drawing and save as HTML format.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
Page page = diagram.Pages[0];       
double pinX = 3, pinY = 3, width = 4, hieght = 4;
using (FileStream fs = new FileStream("image.png", FileMode.Open))
{
    page.AddShape(pinX, pinY, width, hieght, fs);
}
// Save diagram
diagram.Save(dataDir + "AddImageToPage_out.html", new HTMLSaveOptions());

{{< /highlight >}}

