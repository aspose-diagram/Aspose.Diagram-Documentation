---
title: Arbeta med Masters
type: docs
weight: 70
url: /sv/net/working-with-masters/
description: Det här avsnittet förklarar hur man lägger till master eller får masterinformation med Aspose.Diagram.
---
## **Hämtar masterinformation**
En formmästare är ett annat namn för en Visio stencil. Med Aspose.Diagram är det möjligt att hämta information om sidor, kopplingar och även masters. Den här artikeln förklarar hur du får ID och namn från en diagram.

 De[Bemästra](http://www.aspose.com/api/net/diagram/aspose.diagram/master) objekt representerar en[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) objektets master i en diagram. Masters-egenskapen, exponerad av klassen Diagram, stöder en samling Aspose.Diagram.Master-objekt. Den här egenskapen kan användas för att hämta befälhavarnas information, det vill säga master-ID och namn. Använd egenskapen Page.Shapes för att avgöra vilken form som har ärvts av masterformen.
### **Hämtar Master Information Programmeringsexempel**
Följande kodbit hämtar masterinformationen från en diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-RetrieveMasterInfo-RetrieveMasterInfo.cs" >}}
## **Lägg till Master från Stencil of Shapes**
En stencil är en samling former som är associerade med en viss mall Microsoft Office Visio. Med Aspose.Diagram är det möjligt att lägga till valfri formmaster till en ritning från en stencil.
### **Lägg till Master**
 De[Bemästra](http://www.aspose.com/api/net/diagram/aspose.diagram/master) objekt representerar en[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) objektets master i en diagram. AddMaster-metoden, exponerad av klassen Diagram, tillåter att lägga till en master från en stencil. Den erbjuder följande fyra sätt:

- Stencilfilsökväg och master-ID.
- Stencilfilsökväg och huvudnamn.
- Stencilfilström och master-ID.
- Stencilfilström och huvudnamn.
- Lägg till master till diagram från källan diagram
#### **Lägg till masterprogrammeringsexempel**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-AddMasterFromStencil-AddMasterFromStencil.cs" >}}
## **Skapa Master från grunden**
 Aspose.Diagram API gör det möjligt att skapa en[Bemästra](http://www.aspose.com/api/net/diagram/aspose.diagram/master) från grunden utan någon stencil, ritning eller mall. Utvecklare kan anpassa skapandet av Master. AddMaster-metoden, exponerad av klassen Diagram, tillåter att lägga till en master.
### **Skapa masterprogrammeringsexempel**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-CreateMasterFromScratch-CreateMasterFromScratch.cs" >}}
## **Skaffa en Master från filen Visio**
Ibland behöver utvecklare få detaljerna om en Visio ritnings master. Aspose.Diagram API stöder den här funktionen.

 Aspose.Diagram for .NET erbjuder[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)klass som representerar en Visio-ritning. Masters-egenskapen, exponerad av klassen Diagram, stöder en samling Aspose.Diagram.Master-objekt. Den här egenskapen kan användas för att hämta en viss masters detaljer. Klassen MasterCollection exponerar metoderna GetMasterByName och GetMaster som kan anropas för att få ett Master-objekt.
### **Få ett huvudobjekt med ID**
Detta exempel fungerar enligt följande:

1. Skapa ett objekt av klassen Diagram.
1. Ring Diagram.Masters-klassens GetMaster-metod.
#### **Master Object by ID-programmeringsexempel**
Följande exempel visar hur man får en master genom ID från en Visio-ritning.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-GetMasterbyID-GetMasterbyID.cs" >}}
### **Få ett huvudobjekt med namn**
Detta exempel fungerar enligt följande:

1. Skapa ett objekt av klassen Diagram.
1. Ring Diagram.Masters-klassens GetMasterByName-metod.
#### **Master Object by Name Programmeringsexempel**
Följande exempel visar hur man hämtar ett huvudobjekt med namn från en Visio-ritning.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-GetMasterbyName-GetMasterbyName.cs" >}}
## **Kontrollera närvaron av en master i Visio-ritningen**
Aspose.Diagram API stöder kontroll av närvaron av en master i en Visio-ritning. Med MasterCollection-egenskapen kan utvecklare kontrollera om en master är närvarande med sitt namn eller ID.

 Aspose.Diagram for .NET erbjuder[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) klass som representerar en Visio-ritning. Masters-egenskapen, exponerad av klassen Diagram, stöder en samling Aspose.Diagram.Master-objekt. Den här egenskapen kan användas för att kontrollera förekomsten av en viss master. Klassen MasterCollection exponerar IsExist-metoden som kan anropas med masternamnet eller ID-parametern.
### **Kontrollera en masternärvaro med ID**
Detta exempel fungerar enligt följande:

1. Skapa ett objekt av klassen Diagram.
1. Ring Diagram.Masters class' IsExist-metod.
#### **Mästarnärvaro genom ID-programmeringsexempel**
Följande exempel visar hur man kontrollerar närvaron av en master genom ID i en Visio-ritning.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-CheckMasterPresencebyID-CheckMasterPresencebyID.cs" >}}
### **Kontrollera en mästarnärvaro efter namn**
Detta exempel fungerar enligt följande:

1. Skapa ett objekt av klassen Diagram.
1. Ring Diagram.Masters class' IsExist-metod.
#### **Master Presence by Name Programmeringsexempel**
Följande exempel visar hur man kontrollerar en masternärvaro med namn från Visio-ritningen.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Masters-CheckMasterPresencebyName-CheckMasterPresencebyName.cs" >}}
