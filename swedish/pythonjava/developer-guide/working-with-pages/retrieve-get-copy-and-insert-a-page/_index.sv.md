---
title: Hämta, hämta, kopiera och infoga en sida
type: docs
weight: 10
url: /sv/python-java/retrieve-get-copy-and-insert-a-page/
---
## **Hämtar sidinformation**
I Microsoft Visio är sidorna antingen förgrunds- eller bakgrundssidor. För att få sidinformation, till exempel sid-ID och sidnamn, måste du först fastställa om en sida är en bakgrunds- eller förgrundssida.

Objektet `Page` representerar ritytan på en förgrundssida eller en bakgrundssida. Egenskapen Pages som exponeras av klassen `Diagram` stöder en samling av sidobjekt. Den här egenskapen kan användas för att hämta sidinformation.

Använd egenskapen `Page.Background` för att avgöra om en sida är en förgrunds- eller bakgrundssida.

### **Hämta sidinformation Programmeringsexempel**
Följande kodbit hämtar sidornas information från en diagram.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-RetrievePageInfo.py" >}}

## **Hämta sidan Visio från en Diagram**
Ibland behöver utvecklare få en Visio-ritning med siddetaljer. Aspose.Diagram för Python via Java har funktioner som hjälper dem att göra detta.

Aspose.Diagram för Python via Java erbjuder klassen `Diagram` som representerar en Visio-ritning. Egenskapen Pages som exponeras av klassen Diagram stöder en samling av `Page` objekt. Klassen PageCollection exponerar metoden `getPage` som kan anropas för att hämta Page-objekt.

### **Skaffa ett Visio sidobjekt med ID**
Detta exempel fungerar enligt följande:

1. Skapa ett objekt av klassen Diagram.
1. Ring Diagram.Pages-klassens getPage-metod.

Följande exempel visar hur man får ett sidobjekt med id från Visio-ritning.

#### **Hämta sidobjekt med ID-programmeringsexempel**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-GetVisioPagebyID.py" >}}

### **Skaffa ett Visio sidobjekt efter namn**
Detta exempel fungerar enligt följande:

1. Skapa ett objekt av klassen Diagram.
1. Ring Diagram.Pages-klassens GetPage-metod.

#### **Hämta Sidobjekt efter namn Programmeringsexempel**
Följande exempel visar hur man får ett sidobjekt efter namn från Visio-ritning.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-GetVisioPagebyName.py" >}}

## **Kopiera en Visio-sida till en annan Diagram**
Aspose.Diagram för Python via Java API tillåter utvecklare att kopiera och lägga till dess innehåll från den Visio diagram till en annan. Det här hjälpämnet förklarar hur du utför denna uppgift.

Aspose.Diagram för Python via Java API har klassen `Diagram` som representerar en Visio ritning. Egenskapen Pages som exponeras av klassen Diagram stöder en samling av `Page` objekt. Klassen PageCollection exponerar metoden `add` som kan anropas för att lägga till ytterligare ett Page-objekt.

Detta exempel fungerar enligt följande:

1. Skapa ett nytt objekt i klassen Diagram.
1. Ladda ett befintligt Visio diagram i klassobjektet Diagram.
1. Lägg till alla masters från den laddade Visio diagram
1. Hämta sidobjekt från den inlästa diagram (som måste kopieras).
1. Ställ in sidobjektets namn och id.
1. Ta bort den tomma sidan av den nya diagram (valfritt).
1. Anrop add-metoden för klassen PageCollection.
1. Spara den nya diagram i datorlagringen.

### **Kopiera ett Visio Sidprogrammeringsexempel**
Kodexemplet nedan visar hur man kopierar ett Visio sidobjekt till en annan Visio ritning.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-CopyVisioPage.py" >}}

## **Kopiera Visio sida till en annan sidinstans**
Metoden `copy` i klassen `Page` tar en sidinstans att klona.

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page()

# copy page

newPage.copy(diagram.getPages().getPage("Page-1"))

```

## **Infoga en tom sida i en Visio-ritning**
Aspose.Diagram för Python via Java kan infoga en ny tom sida i Microsoft Office Visio ritningen. Det här exemplet beskriver hur du gör det.

Metoden `add`, exponerad av Pages-samlingen, tillåter utvecklare att lägga till en ny tom sida i Visio diagram. Sid-ID bör tilldelas.

### **Infoga ett programmeringsexempel på tom sida**
Följande kodbit infogar en tom sida i Visio-ritningen:

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-InsertBlankPageInVisio.py" >}}

## **Flytta sidposition i Visio-ritningen**
Aspose.Diagram för Python via Java API kan flytta sidpositionen i Visio-ritningen. Metoden `moveTo`, exponerad av klassen `Page`, hjälper utvecklare att flytta sidpositionen.

### **Flytta Sidposition Programmeringsexempel**
MoveTo-medlemmen tar målsideindexet som en parameter för att flytta sidans position i Visio-ritningen:

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page(1)

# move page in the diagram

newPage.moveTo(2)

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX)
```
