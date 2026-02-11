---
title: Gruppera, konvertera och verifiera former
type: docs
weight: 80
url: /sv/net/group-convert-and-verify-shapes/
description: Det här avsnittet förklarar hur du grupperar former med Aspose.Diagram.
---
## **Gruppera flera former tillsammans i Visio-ritningen**
Aspose.Diagram API tillåter utvecklare att gruppera former för att flytta dem alla på en gång. Varje form i en grupp har en unik identitet och har sin egen uppsättning egenskaper. När vi ändrar formateringen av en grupp av former tilldelar den den nya egenskapen till varje form.
### **Hur man grupperar former**
 Koncernmetoden som exponeras av[ShapeCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) klass kan användas för att gruppera former.

Koden nedan visar hur man:

1. Ladda ett prov diagram.
1. initierade en uppsättning av formerna
1. få en viss form genom id.
1. få en annan speciell form genom id.
1. tilldela former till arrayen.
1. gruppera former genom att anropa gruppmetoden.
1. spara diagram
#### **Programmeringsexempel för gruppformer**
Använd följande kod i din .NET-applikation för att gruppera former med Aspose.Diagram for .NET API.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-3");

// Initialize an array of shapes
Aspose.Diagram.Shape[] ss = new Aspose.Diagram.Shape[3];

// Extract and assign shapes to the array
ss[0] = page.Shapes.GetShape(15);
ss[1] = page.Shapes.GetShape(16);
ss[2] = page.Shapes.GetShape(17);

// Mark array shapes as group
page.Shapes.Group(ss);

// Save visio diagram
diagram.Save(dataDir + "GroupShapes_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Konvertera en Visio Shape till andra filformat**
Aspose.Diagram for .NET API tillåter utvecklare att konvertera en enda Visio-form till vilket annat filformat som helst. I den här artikeln tar vi bort alla andra Visio-former från sidan och anpassar sidinställningarna efter källans formstorlek.
### **Konvertera en viss Visio-form**
 Utvecklare kan konvertera en Visio-form till PDF, HTML, Image, SVG och SWF med**ange Visio sparalternativ**.
Den här exempelkoden fungerar enligt följande:

1. Ladda en källa Visio.
1. Skaffa en viss sida.
1. Ta bort bakgrundssidan.
1. Bygg en hashtabell med alla former som innehåller ID och namn.
1. Iterera genom hashtabellen
1. Ta bort alla former från Visio-sidan, utom den specifika.
1. Ställ in sidstorleken.
1. Spara sidan Visio i valfritt filformat som stöds.
#### **Konvertera formprogrammeringsexempel**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram srcVisio = new Diagram(dataDir + "Drawing1.vsdx");

double shapeWidth = 0;
double shapeHeight = 0;

// Get Visio page
Aspose.Diagram.Page srcPage = srcVisio.Pages.GetPage("Page-3");
// Remove background page
srcPage.BackPage = null;

// Get hash table of shapes, it holds id and name
Hashtable remShapes = new Hashtable();
// Hashtable<Long, String> remShapes = new Hashtable<Long, String>();
foreach (Aspose.Diagram.Shape shape in srcPage.Shapes)
    // For the normal shape
    remShapes.Add(shape.ID, shape.Name);

// Iterate through the hash table
foreach (DictionaryEntry shapeEntry in remShapes)
{
    long key = (long)shapeEntry.Key;
    string val = (string)shapeEntry.Value;
    Aspose.Diagram.Shape shape = srcPage.Shapes.GetShape(key);
    // Check of the shape name
    if (val.Equals("GroupShape1"))
    {
        // Move shape to the origin corner
        shapeWidth = shape.XForm.Width.Value;
        shapeHeight = shape.XForm.Height.Value;
        shape.MoveTo(shapeWidth * 0.5, shapeHeight * 0.5);
        // Trim page size
        srcPage.PageSheet.PageProps.PageWidth.Value = shapeWidth;
        srcPage.PageSheet.PageProps.PageHeight.Value = shapeHeight;
    }
    else
    {
        // Remove shape from the Visio page and hash table
        srcPage.Shapes.Remove(shape);
    }
}
remShapes.Clear();

// Specify saving options
Aspose.Diagram.Saving.PdfSaveOptions opts = new Aspose.Diagram.Saving.PdfSaveOptions();
// Set page count to save
opts.PageCount = 1;
// Set starting index of the page
opts.PageIndex = 1;
// Save it
srcVisio.Save(dataDir + "SaveVisioShapeInOtherFormats_out.pdf", opts);

{{< /highlight >}}

### **Konvertera Visio Shape till PDF**
ToPdf-metoden för Shape-klassen gör det möjligt att konvertera en form till formatet PDF.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Konvertera Visio Shape till HTML**
ToHTML-metoden för Shape-klassen gör det möjligt att konvertera en form till formatet HTML.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();

// save a shape in the PDF format

diagram.Pages[0].Shapes.GetShape(59).ToHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}
## **Kontrollera om två Visio-former är anslutna eller limmade**
 Aspose.Diagram for .NET API låter utvecklare verifiera att de två Visio-formerna är limmade eller sammankopplade. Tidigare har vi sett hur vi kan ansluta eller limma två former i dessa hjälpämnen:[Lägg till och anslut Visio Former](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) och[Limma former inuti behållaren](/diagram/sv/net/working-with-shapes-gluing/).
### **Verifiering av de anslutna eller limmade formerna**
 De[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class erbjuder egenskaperna IsGlued och IsConnected för att avgöra om två former är limmade eller sammankopplade.
#### **Verifiering av programmeringsprov för anslutna eller limmade former**
Följande kod verifierar om två former är sammankopplade eller limmade.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Set two shape ids
long ShapeIdOne = 15;
long ShapeIdTwo = 16;

// Get Visio page by name
Page page = diagram.Pages.GetPage("Page-3");

// Get Visio shapes by ids
Shape ShapedOne = page.Shapes.GetShape(ShapeIdOne);
Shape ShapedTwo = page.Shapes.GetShape(ShapeIdTwo);

// Determine whether shapes are connected
bool connected = ShapedOne.IsConnected(ShapedTwo);
Console.WriteLine("Shapes are connected: " + connected);

// Determine whether shapes are glued
bool glued = ShapedOne.IsGlued(ShapedTwo);
Console.WriteLine("Shapes are Glued: " + glued);

{{< /highlight >}}

## **Verifiera om Visio-formen är i en grupp av former**
Aspose.Diagram for .NET API tillåter utvecklare att verifiera att Visio-formen är i en grupp av former eller inte.
### **Verifiering av form i gruppen av former**
De[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)class erbjuder IsInGroup-egenskaper för att avgöra om Visio-formen är i en gruppform.
#### **Verifiering av form i gruppen av formprogrammeringsexempel**
Följande kodbit verifierar om formen är i en gruppform.


{{< highlight csharp >}}
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();
// Call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get a sub-shape by page name, group shape ID, and then sub-shape ID
Shape shape = diagram.Pages.GetPage("Page-3").Shapes.GetShape(13).Shapes.GetShape(2);
Console.WriteLine("Is it in a Group: " + shape.IsInGroup());
{{< /highlight >}}

