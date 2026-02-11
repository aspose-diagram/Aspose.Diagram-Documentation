---
title: Arbeta med hyperlänkar
type: docs
weight: 160
url: /sv/net/working-with-hyperlinks/
description: Det här avsnittet förklarar hur du lägger till eller hämtar hyperlänk i en Visio-form med Aspose.Diagram.
---
## **Lägg till hyperlänk till en Visio-form**
Microsoft Office Visio stöder att lägga till hyperlänkar till valfri form. Hyperlänkarna kan länka till en annan sida eller form i den aktuella ritningen, en sida eller form i en annan ritning, ett annat dokument än en Visio-ritning, en webbplats, FTP-sida eller e-postadress. Utvecklare kan använda Aspose.Diagram API för att enkelt lägga till hyperlänkar till en Visio-form.

 I den flersidiga Visio-ritningen kan hyperlänkar navigera dig från en form till många andra typer av länkar.[HyperlinkCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/hyperlinkcollection) utsatt av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class erbjuder Lägg till metod som kan användas för att lägga till en forms hyperlänk.

För att identifiera fastigheter i Microsoft Office Visio:

1. I en Visio diagram högerklickar du på en form.
1.  Välj**Hyperlänk.**
1. Ange befintliga egenskaper
1.  Tryck**OK** knapp

**En forms hyperlänksdata, som ses i Microsoft Visio**

![todo:image_alt_text](working-with-hyperlinks_1.png)
### **Lägg till hyperlänksprogrammeringsexempel**
Kodavsnittet nedan lägger till forms hyperlänkdata.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Hyperlinks();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(2);

// Initialize Hyperlink object
Hyperlink hyperlink = new Hyperlink();
// Set address value
hyperlink.Address.Value = "http:// Www.google.com/";
// Set sub address value
hyperlink.SubAddress.Value = "Sub address here";
// Set description value
hyperlink.Description.Value = "Description here";
// Set name
hyperlink.Name = "MyHyperLink";

// Add hyperlink to the shape
shape.Hyperlinks.Add(hyperlink);            
// Save diagram to local space
diagram.Save(dataDir + "AddHyperlinkToShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Hämta hyperlänkdata för Visio-formerna**
Utvecklare kan hämta alla hyperlänkar från en Visio-form på samma sätt som de[läs Visio formdata](https://docs.aspose.com/diagram/net/load-or-create-a-visio-drawing/) använder sig av[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

I den flersidiga Visio-ritningen kan hyperlänkar navigera dig från en form till många andra typer av länkar.[HyperlinkCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/hyperlinkcollection) utsatt av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass tillåter utvecklare att hämta hyperlänkar.

För att identifiera fastigheter i Microsoft Office Visio:

1. I en diagram högerklickar du på en form.
1.  Välj**Hyperlänk.**

Alla befintliga egenskaper listas i dialogrutan.
**En forms hyperlänksdata, som ses i Microsoft Visio**

![todo:image_alt_text](working-with-hyperlinks_1.png)

**Ett konsolfönster som visar formdatautmatningen**

![todo:image_alt_text](working-with-hyperlinks_3.png)
### **Få hyperlänksprogrammeringsexempel**
Kodavsnittet nedan läser shapes hyperlänkdata.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Hyperlinks();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);
// Iterate through the hyperlinks
foreach (Aspose.Diagram.Hyperlink hyperlink in shape.Hyperlinks)
{
    Console.WriteLine("Address: " + hyperlink.Address.Value);
    Console.WriteLine("Sub Address: " + hyperlink.SubAddress.Value);
    Console.WriteLine("Description: " + hyperlink.Description.Value);
}       

{{< /highlight >}}

