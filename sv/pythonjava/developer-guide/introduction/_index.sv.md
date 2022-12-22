---
title: Introduktion
type: docs
weight: 10
url: /sv/net/introduction/
description: Introduktion av Aspose.Diagram bibliotek.
---
## **Hämta dokumentinformationen Visio från biblioteket Aspose.Diagram for .NET**
Microsoft Visio sparar information om åtgärder som vidtagits på en diagram i filen. Till exempel, tid och datum då dokumentet skapades, senast det redigerades, skrevs ut eller sparades, sparas med filen. Information om vilken version av Microsoft Visio som skapats och senast redigerade filen sparas också.

Den här artikeln förklarar hur du hämtar den informationen.
### **Bestämma versionen av Microsoft Visio som har skapats, redigerats och sparats ett dokument**
 Egenskapen Version exponerad av[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/)klassen och egenskapen BuildNumberCreated som exponeras av klassen DocumentProperties används för att fastställa versionen och det fullständiga byggnumret för instansen Microsoft Visio som används för att skapa dokumentet.

 Egenskapen BuildNumberEdited exponerad av[Dokument egenskaper](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties) klass används för att fastställa det fullständiga byggnumret för instansen Microsoft Visio som används för att redigera dokumentet.

Egenskaperna TimeCreated, TimeEdited, TimePrinted och TimeSaved som exponeras av klassen DocumentProperties används för att bestämma tiden då dokumentet Microsoft Visio skapades, senast redigerades, senast skrevs ut och senast sparades.

Du kan också ställa in dessa egenskaper för att ändra informationen i filen. Kodexemplen nedan visar hur man hämtar information om vad som skapade filen samt när den skapades, redigerades, skrevs ut och sparades.
#### **Programmeringsexempel**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-GetLibraryVersion-GetLibraryVersion.cs" >}}
## **Skriver Visio Dokumentsammanfattningsinformation**
Microsoft Visio låter dig definiera ett antal egenskaper för dokumentsammanfattningsinformation för att hjälpa dig och dina kollegor att identifiera en diagram. Sammanfattningsegenskaper, till exempel titel, ämne, författare och beskrivning, gör filen lättare att hitta vid sökning och lättare att känna igen när bläddra i filer.
### **Skriver Microsoft Visio Dokumentsammanfattning Info**
Klassen DocumentProperties exponerar ett antal egenskaper för att ställa in eller hämta en Visio diagram sammanfattningsinformation. Aspose.Diagram for .NET kan uppdatera ritningssammanfattningsinformationen och sedan skriva tillbaka ritningsfilen till VDX.

{{% alert color="primary" %}} 

Observera att du inte kan ställa in värden mot**Ansökan**och**Producent**fält, eftersom Aspose Ltd. och Aspose.Diagram for .NET xxx kommer att visas mot dessa fält.

{{% /alert %}} 

Så här uppdaterar du ritningssammanfattningsinformationen för en befintlig VDX- eller VSD-fil:

1.  Skapa en instans av[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/) klass.
1.  Ställ in egenskaper exponerade av[Diagram.DocumentProps](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/properties/documentprops) för att definiera sammanfattningsinformationen för ritningsfilen Visio.
1. Ring Diagram-klassens Spara-metod för att skriva Visio-ritningsfilen till VDX.

Kontrollera sammanfattningsinformationen:

1. Öppna utdatafilen VDX i Microsoft Visio.
1. Välj Info från Arkiv-menyn.
#### **Skriver Visio Dokumentsammanfattningsinformation Programmeringsexempel**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-SetVisioProperties-SetVisioProperties.cs" >}}
## **Upptäck filformatet Visio**
Genom att använda Aspose.Diagram for .NET API kan utvecklare upptäcka formatet på filen Visio innan den öppnas eftersom filtillägget inte garanterar att filinnehållet är lämpligt.
### **Upptäck formatprogrammeringsexempel**
Följande exempelkod illustrerar hur du upptäcker ett filformat (med sökvägen eller strömmen) och kontrollerar dess tillägg.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-DetectVisioFileFormat-DetectVisioFileFormat.cs" >}}
