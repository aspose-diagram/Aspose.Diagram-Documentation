---
title: Hämta, hämta, kopiera och infoga en sida
type: docs
weight: 10
url: /sv/net/retrieve-get-copy-and-insert-a-page/
description: Det här avsnittet förklarar hur man infogar en sida, kopierar en sida eller får sidinformation med Aspose.Diagram.
---
## **Hämtar sidinformation**
I Microsoft Visio är sidorna antingen förgrunds- eller bakgrundssidor. För att få sidinformation, till exempel sid-ID och sidnamn, måste du först fastställa om en sida är en bakgrunds- eller förgrundssida.

 De[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page)objekt representerar ritytan på en förgrundssida eller en bakgrundssida. Sidornas egendom exponerad av[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) klass stöder en samling av Aspose.Diagram.Page-objekt. Den här egenskapen kan användas för att hämta sidinformation.

Använd egenskapen Page.Background för att avgöra om en sida är en förgrunds- eller bakgrundssida.
### **Hämta sidinformation Programmeringsexempel**
Följande kodbit hämtar sidornas information från en diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VDX file
Diagram vdxDiagram = new Diagram(dataDir + "RetrievePageInfo.vdx");

foreach (Aspose.Diagram.Page page in vdxDiagram.Pages)
{
    // Checks if current page is a background page
    if (page.Background == Aspose.Diagram.BOOL.True)
    {
        // Display information about the background page
        Console.WriteLine("Background Page ID : " + page.ID);
        Console.WriteLine("Background Page Name : " + page.Name);
    }
    else
    {
        // Display information about the foreground page
        Console.WriteLine("\nPage ID : " + page.ID);
        Console.WriteLine("Universal Name : " + page.NameU);
        Console.WriteLine("ID of the Background Page : " + page.BackPage);
    }
}

{{< /highlight >}}

## **Hämta sidan Visio från en Diagram**
Ibland behöver utvecklare få en Visio-ritning med siddetaljer. Aspose.Diagram har funktioner som hjälper dem att göra detta.

 Aspose.Diagram for .NET erbjuder[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) klass som representerar en Visio-ritning. Egenskapen Pages som exponeras av klassen Diagram stöder en samling av Aspose.Diagram.Page-objekt. Klassen PageCollection exponerar GetPage-metoden som kan anropas för att hämta Page-objekt.
### **Skaffa ett Visio sidobjekt med ID**
Detta exempel fungerar enligt följande:

1. Skapa ett objekt av klassen Diagram.
1. Ring Diagram.Pages-klassens GetPage-metod.

Följande exempel visar hur man får ett sidobjekt med id från Visio-ritning.
#### **Hämta sidobjekt med ID-programmeringsexempel**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page id
int pageid = 2;
// Get page object by id
Page page2 = diagram.Pages.GetPage(pageid);

{{< /highlight >}}

### **Skaffa ett Visio sidobjekt efter namn**
Detta exempel fungerar enligt följande:

1. Skapa ett objekt av klassen Diagram.
1. Ring Diagram.Pages-klassens GetPage-metod.
#### **Hämta Sidobjekt efter namn Programmeringsexempel**
Följande exempel visar hur man får ett sidobjekt efter namn från Visio-ritning.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page name
string pageName = "Flow 2";
// Get page object by name
Page page2 = diagram.Pages.GetPage(pageName);

{{< /highlight >}}

## **Kopiera en Visio-sida till en annan Diagram**
Aspose.Diagram for .NET API tillåter utvecklare att kopiera och lägga till dess innehåll från den ena Visio diagram till en annan. Det här hjälpämnet förklarar hur du utför denna uppgift.

 Aspose.Diagram for .NET API har[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) klass som representerar en Visio-ritning. Egenskapen Pages som exponeras av klassen Diagram stöder en samling av Aspose.Diagram.Page-objekt. Klassen PageCollection visar Add-metoden som kan anropas för att lägga till ytterligare ett Page-objekt.

Detta exempel fungerar enligt följande:

1. Skapa ett nytt objekt i klassen Diagram.
1. Ladda ett befintligt Visio diagram i klassobjektet Diagram.
1. Lägg till alla masters från den laddade Visio diagram
1. Hämta sidobjekt från den inlästa diagram (som måste kopieras).
1. Ställ in sidobjektets namn och id.
1. Ta bort den tomma sidan av den nya diagram (valfritt).
1. Anrop Add-metoden för klassen PageCollection.
1. Spara den nya diagram i datorlagringen.
### **Kopiera ett Visio Sidprogrammeringsexempel**
Kodexemplet nedan visar hur man kopierar ett Visio sidobjekt till en annan Visio ritning.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram NewDigram = new Diagram();

// Load source diagram
Diagram dgm = new Diagram(dataDir + "Drawing1.vsdx");
// Add all masters from the source Visio diagram
foreach (Master master in dgm.Masters)
    NewDigram.Masters.Add(master);

// Get page object
Aspose.Diagram.Page SrcPage = dgm.Pages.GetPage("Page-1");
// Set name
SrcPage.Name = "new page";

// It calculates max page id
int max = 0;
if (NewDigram.Pages.Count != 0)
    max = NewDigram.Pages[0].ID;

for (int i = 1; i < NewDigram.Pages.Count; i++)
{
    if (max < NewDigram.Pages[i].ID)
        max = NewDigram.Pages[i].ID;
}
            
// Set max page ID 
int MaxPageId = max;
// Set page ID
SrcPage.ID = MaxPageId + 1;

// Add page from the source diagram
NewDigram.Pages.Add(SrcPage);
// Remove first empty page
NewDigram.Pages.Remove(NewDigram.Pages[0]);
// Save diagram
NewDigram.Save(dataDir + "CopyVisioPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Kopiera Visio sida till en annan sidinstans**
Kopieringsmetoden för klassen Page tar en sidinstans att klona.

**C#**

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page();

// copy page

newPage.Copy(diagram.Pages.GetPage("Page-1"));

{{< /highlight >}}
## **Infoga en tom sida i en Visio-ritning**
[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) kan infoga en ny tom sida i Microsoft Office Visio ritningen. Det här exemplet beskriver hur du gör det.

Add-metoden, exponerad av Pages-samlingen, tillåter utvecklare att lägga till en ny tom sida i Visio diagram. Sid-ID bör tilldelas.
### **Infoga ett programmeringsexempel på tom sida**
Följande kodbit infogar en tom sida i Visio-ritningen:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// It calculates max page id
int max = 0;
if (diagram.Pages.Count != 0)
    max = diagram.Pages[0].ID;

for (int i = 1; i < diagram.Pages.Count; i++)
{
    if (max < diagram.Pages[i].ID)
        max = diagram.Pages[i].ID;
}

// Set max page ID
int MaxPageId = max;

// Initialize a new page object
Page newPage = new Page();
// Set name
newPage.Name = "new page";
// Set page ID
newPage.ID = MaxPageId + 1;

// Or try the Page constructor
// Page newPage = new Page(MaxPageId + 1);

// Add a new blank page
diagram.Pages.Add(newPage);

// Save diagram
diagram.Save(dataDir + "InsertBlankPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Flytta sidposition i Visio-ritningen**
Aspose.Diagram for .NET API kan flytta sidpositionen i Visio-ritningen. MoveTo-metoden, exponerad av klassen Page, hjälper utvecklare att flytta sidpositionen.
### **Flytta Sidposition Programmeringsexempel**
MoveTo-medlemmen tar målsideindexet som en parameter för att flytta sidans position i Visio-ritningen:

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.MoveTo(2);

diagram.Save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
