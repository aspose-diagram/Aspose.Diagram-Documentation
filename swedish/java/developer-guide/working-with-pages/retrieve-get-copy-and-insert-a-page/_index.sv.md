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

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-RetrievePageInfo-RetrievePageInfo.java" >}}
## **Hämta sidan Visio från en Diagram**
Ibland behöver utvecklare få en Visio-ritning med siddetaljer. Aspose.Diagram har funktioner som hjälper dem att göra detta.

 Aspose.Diagram for Java erbjuder[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) klass som representerar en Visio-ritning. Egenskapen Pages som exponeras av klassen Diagram stöder en samling av Aspose.Diagram.Page-objekt. Klassen PageCollection exponerar GetPage-metoden som kan anropas för att hämta Page-objekt.
### **Skaffa ett Visio sidobjekt med ID**
Detta exempel fungerar enligt följande:

1. Skapa ett objekt av klassen Diagram.
1. Ring Diagram.Pages-klassens GetPage-metod.

Följande exempel visar hur man får ett sidobjekt med id från Visio-ritning.
#### **Hämta sidobjekt med ID-programmeringsexempel**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-GetVisioPagebyID-GetVisioPagebyID.java" >}}
### **Skaffa ett Visio sidobjekt efter namn**
Detta exempel fungerar enligt följande:

1. Skapa ett objekt av klassen Diagram.
1. Ring Diagram.Pages-klassens GetPage-metod.
#### **Hämta Sidobjekt efter namn Programmeringsexempel**
Följande exempel visar hur man får ett sidobjekt efter namn från Visio-ritning.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-GetVisioPagebyName-GetVisioPagebyName.java" >}}
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

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-CopyVisioPage-CopyVisioPage.java" >}}
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

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Pages-InsertBlankPageInVisio-InsertBlankPageInVisio.java" >}}
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
