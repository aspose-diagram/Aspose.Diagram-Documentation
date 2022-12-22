---
title: Introduktion
type: docs
weight: 10
url: /sv/java/introduction/
---
{{% alert color="primary" %}} 

Microsoft Visio sparar information om åtgärder som vidtagits på en diagram i filen. Till exempel, tid och datum då dokumentet skapades, senast det redigerades, skrevs ut eller sparades, sparas med filen. Information om vilken version av Microsoft Visio som skapats och senast redigerade filen sparas också.

Den här artikeln förklarar hur du hämtar den informationen.

{{% /alert %}} 
## **Hämta versionen av biblioteket Aspose.Diagram for Java**
 GetVersion()-memetoden exponerad av[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) klass och metoden getBuildNumberCreated() som exponeras av[Dokument egenskaper](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) klass används för att fastställa versionen och det fullständiga byggnumret för instansen Microsoft Visio som används för att skapa dokumentet.
### **Bestämma versionen av Microsoft Visio som har skapats, redigerats och sparats ett dokument**
 Metoden getBuildNumberEdited() exponerad av[Dokument egenskaper](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) klass används för att fastställa det fullständiga byggnumret för instansen Microsoft Visio som används för att redigera dokumentet.

Metoderna getTimeCreated(), getTimeEdited(), getTimePrinted() och getTimeSaved() exponerade av[Dokument egenskaper](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties) klass används för att bestämma tiden då dokumentet Microsoft Visio skapades, senast redigerades, senast skrevs ut och senast sparades.

Du kan också ställa in dessa egenskaper för att ändra informationen i filen.

Kodexemplen nedan visar hur man hämtar information om vad som skapade filen samt när den skapades, redigerades, skrevs ut och sparades.

**Koden matas ut i ett konsolfönster** 

![todo:image_alt_text](introduction_1.png)
#### **Programmeringsexempel**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-GetLibraryVersion-GetLibraryVersion.java" >}}
## **Skriver Microsoft Visio Dokumentsammanfattning Info**
Microsoft Visio låter dig definiera ett antal egenskaper för dokumentsammanfattningsinformation för att hjälpa dig och dina kollegor att identifiera en diagram. Sammanfattningsegenskaper, till exempel titel, ämne, författare och beskrivning, gör filen lättare att hitta när du söker och lättare att känna igen när du surfar filer.

 De[Dokument egenskaper](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentProperties)klass exponerar ett antal egenskaper för att ställa in eller få en Microsoft Visio diagram sammanfattande information. Aspose.Diagram for Java kan uppdatera ritningssammanfattningsinformationen och sedan skriva tillbaka ritningsfilen till VDX.

{{% alert color="primary" %}} 

Observera att du inte kan ställa in värden mot**Ansökan**och**Producent**fält, eftersom Aspose Ltd. och Aspose.Diagram for Java xxx kommer att visas mot dessa fält.

{{% /alert %}} 
### **Skriver Microsoft Visio Dokumentsammanfattning Info**
Så här uppdaterar du ritningssammanfattningsinformationen för en befintlig VDX- eller VSD-fil:

1.  Skapa en instans av[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) klass.
1. Ställ in egenskaper som exponeras med metoden Diagram.getDocumentProps() för att definiera sammanfattningsinformationen för ritningsfilen Visio.
1. Anropa Diagram-klassens save()-metod för att skriva ritningsfilen Visio till VDX.

Kontrollera sammanfattningsinformationen:

1. Öppna utdatafilen VDX i Microsoft Visio.
1.  Väljer**Info** från**Fil** meny.

**Infodialogen som visar den uppdaterade sammanfattningsinformationen** 

![todo:image_alt_text](introduction_2.png)
#### **Programmeringsexempel**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-SetVisioProperties-SetVisioProperties.java" >}}
## **Upptäck formatet för en Visio-fil**
 Använder sig av[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/)API, kan utvecklare upptäcka formatet på filen Visio innan den öppnas eftersom filtillägget inte garanterar att filinnehållet är lämpligt.
### **Upptäck formatprogrammeringsexempel**
Följande exempelkod illustrerar hur du upptäcker ett filformat (med sökvägen eller strömmen) och kontrollerar dess tillägg.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-DetectVisioFileFormat-DetectVisioFileFormat.java" >}}
## **Upptäck formatet för en Visio-fil från en InputStream**
Med hjälp av Aspose.Diagram for Java API kan utvecklare upptäcka formatet för en Visio-fil genom att skicka en indataström. DetectFileFormat-metoden i klassen FileFormatUtil kan användas för att uppnå detta.
### **Upptäck format från ett InputStream-programmeringsexempel**
Följande exempelkod illustrerar hur man upptäcker ett filformat med hjälp av en indataström.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-DetectFormatfromInputStream-DetectFormatfromInputStream.java" >}}
