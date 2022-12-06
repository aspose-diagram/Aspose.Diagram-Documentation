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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-RetrievePageInfo-RetrievePageInfo.cs" >}}
## **Hämta sidan Visio från en Diagram**
Ibland behöver utvecklare få en Visio-ritning med siddetaljer. Aspose.Diagram har funktioner som hjälper dem att göra detta.

 Aspose.Diagram for .NET erbjuder[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) klass som representerar en Visio-ritning. Egenskapen Pages som exponeras av klassen Diagram stöder en samling av Aspose.Diagram.Page-objekt. Klassen PageCollection exponerar GetPage-metoden som kan anropas för att hämta Page-objekt.
### **Skaffa ett Visio sidobjekt med ID**
Detta exempel fungerar enligt följande:

1. Skapa ett objekt av klassen Diagram.
1. Ring Diagram.Pages-klassens GetPage-metod.

Följande exempel visar hur man får ett sidobjekt med id från Visio-ritning.
#### **Hämta sidobjekt med ID-programmeringsexempel**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-GetVisioPagebyID-GetVisioPagebyID.cs" >}}
### **Skaffa ett Visio sidobjekt efter namn**
Detta exempel fungerar enligt följande:

1. Skapa ett objekt av klassen Diagram.
1. Ring Diagram.Pages-klassens GetPage-metod.
#### **Hämta Sidobjekt efter namn Programmeringsexempel**
Följande exempel visar hur man får ett sidobjekt efter namn från Visio-ritning.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-GetVisioPagebyName-GetVisioPagebyName.cs" >}}
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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-CopyVisioPage-CopyVisioPage.cs" >}}
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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Pages-InsertBlankPageInVisio-InsertBlankPageInVisio.cs" >}}
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
