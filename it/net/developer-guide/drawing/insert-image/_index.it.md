---
title: Inserisci immagine
type: docs
weight: 70
url: /it/net/drawing/insert-image
description: Questa sezione spiega come inserire un'immagine in una pagina visio con Aspose.Diagram. Supporto utilizzando C# per inserire l'immagine e salvarla come pdf, svg, html, immagine, xps e altri formati.
---
 Il[Pagina](http://www.aspose.com/api/net/diagram/aspose.diagram/page)oggetto rappresenta l'area di disegno di una pagina in primo piano o di una pagina di sfondo. La proprietà Pages esposta da[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class supporta una raccolta di oggetti Aspose.Diagram.Page.

## **Inserisci l'immagine in Visio**
Aspose.Diagram for .NET API consente agli sviluppatori di inserire una forma di immagine in una pagina. L'esempio di codice seguente mostra come inserire un'immagine in un disegno Visio.


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


## **Inserisci l'immagine in SVG**
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


## **Inserisci l'immagine in PNG**
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


## **Inserisci l'immagine in PDF**
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


## **Inserisci l'immagine in HTML**
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

