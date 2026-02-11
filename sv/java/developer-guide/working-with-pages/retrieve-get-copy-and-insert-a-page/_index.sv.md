---
title: Hämta, hämta, kopiera och infoga en sida
type: docs
weight: 10
url: /sv/java/retrieve-get-copy-and-insert-a-page/
---
## **Hämtar sidinformation**
I Microsoft Visio är sidorna antingen förgrunds- eller bakgrundssidor. För att få sidinformation, till exempel sid-ID och sidnamn, måste du först fastställa om en sida är en bakgrunds- eller förgrundssida.

 De[Sida](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)objekt representerar ritytan på en förgrundssida eller en bakgrundssida. Sidornas egendom exponerad av[Diagram](https://reference.aspose.com/diagram/java) klass stöder en samling av Aspose.Diagram.Page-objekt. Den här egenskapen kan användas för att hämta sidinformation.

Använd egenskapen Page.Background för att avgöra om en sida är en förgrunds- eller bakgrundssida.

Bilden nedan visar utdata från kodavsnitten i den här artikeln.

**En konsol som visar utgången.** 

![todo:image_alt_text](retrieve-get-copy-and-insert-a-page_1.png)
### **Hämta sidinformation Programmeringsexempel**
Följande kodbit hämtar sidornas information från en diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrievePageInfo.class);

//Call the diagram constructor to load diagram
Diagram diagram = new Diagram(dataDir+ "RetrievePageInfo.vdx");

for (Page page : (Iterable<Page>) diagram.getPages())
{
    //Checks if current page is a background page
    if (page.getBackground() == com.aspose.diagram.BOOL.TRUE)
    {
        //Display information about the background page
        System.out.println("Background Page ID : " + page.getID());
        System.out.println("Background Page Name : " + page.getName());
    }
    else
    {
        //Display information about the foreground page
        System.out.println("\nPage ID : " + page.getID());
        System.out.println("Universal Name : " + page.getNameU());
        System.out.println("ID of the Background Page : " + page.getBackPage());
    }
}

{{< /highlight >}}

## **Hämta sidan Visio från en Diagram**
Ibland behöver utvecklare få en Visio-ritning med siddetaljer. Aspose.Diagram har funktioner som hjälper dem att göra detta.

 Aspose.Diagram for Java erbjuder[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) klass som representerar en Visio-ritning. Egenskapen Pages som exponeras av klassen Diagram stöder en samling av Aspose.Diagram.Page-objekt. Klassen PageCollection exponerar GetPage-metoden som kan anropas för att hämta Page-objekt.
### **Skaffa ett Visio sidobjekt med ID**
Detta exempel fungerar enligt följande:

1. Skapa ett objekt av klassen Diagram.
1. Ring Diagram.Pages-klassens GetPage-metod.

Följande exempel visar hur man får ett sidobjekt med id från Visio-ritning.
#### **Hämta sidobjekt med ID-programmeringsexempel**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetVisioPagebyID.class); 
// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page id
int pageid = 2;
// Get page object by id
Page page2 = diagram.getPages().getPage(pageid);

{{< /highlight >}}

### **Skaffa ett Visio sidobjekt efter namn**
Detta exempel fungerar enligt följande:

1. Skapa ett objekt av klassen Diagram.
1. Ring Diagram.Pages-klassens GetPage-metod.
#### **Hämta Sidobjekt efter namn Programmeringsexempel**
Följande exempel visar hur man får ett sidobjekt efter namn från Visio-ritning.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetVisioPagebyName.class);     
// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page name
String pageName = "Flow 2";
// Get page object by name
Page page2 = diagram.getPages().getPage(pageName);

{{< /highlight >}}

## **Kopiera en Visio-sida till en annan Diagram**
Aspose.Diagram for Java API tillåter utvecklare att kopiera och lägga till dess innehåll från den ena Visio diagram till en annan. Det här hjälpämnet förklarar hur du utför denna uppgift.

 Aspose.Diagram for Java API har[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) klass som representerar en Visio-ritning. Egenskapen Pages som exponeras av klassen Diagram stöder en samling av Aspose.Diagram.Page-objekt. Klassen PageCollection visar Add-metoden som kan anropas för att lägga till ytterligare ett Page-objekt.

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


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CopyVisioPage.class);
        
// Call the diagram constructor to load diagram from a VSD file
Diagram originalDiagram = new Diagram(dataDir + "Drawing1.vsd");

// initialize the new visio diagram
Diagram newDiagram = new Diagram();

// add all masters from the source Visio diagram
MasterCollection originalMasters = originalDiagram.getMasters();
for (Master master : (Iterable<Master>) originalMasters) {
   newDiagram.addMaster(originalDiagram, master.getName());
}

// get the page object from the original diagram
Page SrcPage = originalDiagram.getPages().getPage("Page-1");
// set page name
SrcPage.setName("new page");
        
// it calculates max page id
int max = 0;
if (newDiagram.getPages().getCount() != 0)
    max = newDiagram.getPages().get(0).getID();

for (int i = 1; i < newDiagram.getPages().getCount(); i++)
{
    if (max < newDiagram.getPages().get(i).getID())
        max = newDiagram.getPages().get(i).getID();
}
       
int MaxPageId = max;
// set page id
SrcPage.setID(MaxPageId);
// add reference of the original diagram page
newDiagram.getPages().add(SrcPage);

// remove first empty page
newDiagram.getPages().remove(newDiagram.getPages().get(0));

// save diagram in VDX format
newDiagram.save(dataDir + "CopyVisioPage_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Kopiera Visio sida till en annan sidinstans**
Kopieringsmetoden för klassen Page tar en sidinstans att klona.

**Java**

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page();

// copy page

newPage.copy(diagram.getPages().getPage("Page-1"));

{{< /highlight >}}
## **Infoga en tom sida i en Visio-ritning**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) kan infoga en ny tom sida i Microsoft Office Visio ritningen. Det här exemplet beskriver hur du gör det.

Add-metoden, exponerad av Pages-samlingen, tillåter utvecklare att lägga till en ny tom sida i Visio diagram. Sid-ID bör tilldelas.
### **Infoga ett programmeringsexempel på tom sida**
Följande kodbit infogar en tom sida i Visio-ritningen:


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(InsertBlankPageInVisio.class);   
// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
        
// it calculates max page id
int max = 0;
if (diagram.getPages().getCount() != 0)
    max = diagram.getPages().get(0).getID();

for (int i = 1; i < diagram.getPages().getCount(); i++)
{
    if (max < diagram.getPages().get(i).getID())
        max = diagram.getPages().get(i).getID();
}
        
// Initialize a new page object
Page newPage = new Page();
// Set name
newPage.setName("new page");
// Set page ID
newPage.setID(max + 1);

// Or try the Page constructor
// Page newPage = new Page(MaxPageId + 1);

// Add a new blank page
diagram.getPages().add(newPage);

// Save diagram
diagram.save(dataDir + "InsertBlankPageInVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Flytta sidposition i Visio-ritningen**
Aspose.Diagram for Java API kan flytta sidpositionen i Visio-ritningen. MoveTo-metoden, exponerad av klassen Page, hjälper utvecklare att flytta sidpositionen.
### **Flytta Sidposition Programmeringsexempel**
MoveTo-medlemmen tar målsideindexet som en parameter för att flytta sidans position i Visio-ritningen:

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.moveTo(2);

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
