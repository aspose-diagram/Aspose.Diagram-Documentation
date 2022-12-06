---
title: Ställ in Visio Shapes XForm, Line och Fill Data
type: docs
weight: 20
url: /sv/net/set-visio-shape-s-xform-line-and-fill-data/
description: Det här avsnittet förklarar hur du ställer in formens stil inklusive dess linjedata och fyllningsdata med Aspose.Diagram.
---
## **Ställa in XForm-data**
 XForm-elementet är en del av XML-schemat Microsoft Visio. XForm anger en forms position, till exempel bredd, höjd, rotation och om formen har vänts. De[XForm](http://www.aspose.com/api/net/diagram/aspose.diagram/xform) egendom, exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass, stöder objektet Aspose.Diagram.XForm. XForm-egenskapen kan användas för att hämta eller uppdatera en forms XForm-data. Kodexemplen i den här artikeln ändrar PinX (X-koordinat) och PinY (Y-koordinat) XForm-värden för att flytta formerna på sidan.

Processen för att uppdatera XForm-data är:

1. Ladda en diagram.# Hitta en viss form.# Uppdatera formens XForm-data.
1. Spara diagram.
### **Programmeringsexempel**
Kodavsnittet nedan visar hur du uppdaterar en forms XForm-data. Koden letar efter en process för formnamn, med form-ID 1, och ställer in dess X- och Y-koordinater till 5.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetXFormdata-SetXFormdata.cs" >}}
## **Ställ in Visio Shape's Line Data**
Former kan formateras på flera sätt. Den här artikeln visar hur du anger en linjes attribut.

Microsoft Visio låter användare formatera linjer på olika sätt. Aspose.Diagram for .NET stöder:

- Vikt: en linjes tjocklek.
- Färg: ställ in formens linjefärg.
- Linjefärgstransparens: ställ in formens linjefärgtransparens i procent.
- Mönster: definierar om linjen är heldragen, streckad eller har ett annat mönster.
- Avrundning: radien på hörnen.
- Start- och slutpilar: ange om linjen har pilar.
- Början och slutet pilstorlekar: ställ in pilstorlekarna.
- Cap: avrundningen av linjen slutar.
### **Ändra linjefärg, vikt, strecktyp, transparens, avrundning, piltyp och pilstorlek för en forms kant**
 De[Linje](http://www.aspose.com/api/net/diagram/aspose.diagram/line) egendom, exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)klass, stöder objektet Aspose.Diagram.Line. Den här egenskapen kan användas för att hämta eller uppdatera en forms linjedata.
#### **Linjedataprogrammeringsexempel**
Följande kodbit uppdaterar formens linjedata.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetLineData-SetLineData.cs" >}}
## **Ställ in Visio Shape's Fill Data**
 Former kan formateras på flera sätt. Det här avsnittet beskriver hur du anger en forms fyllning. Microsoft Office Visio låter användare formatera fyllningar på olika sätt. De[Fylla](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) klass av Aspose.Diagram for .NET API stöder inställning:

- Bakgrunds- och förgrundsfärger.
- Genomskinlighet.
- Fyllningsmönster.
- Skuggor.
### **Ställa in fyllningsvärden**
 Fill-egenskapen, exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass, stödjer[Aspose.Diagram.Fill](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) objekt. Fill-egenskapen kan användas för att hämta eller uppdatera en forms fyllningsdata.
#### **Fyll i dataprogrammeringsexempel**
Följande kodavsnitt uppdaterar en forms fyllningsdata. Koden letar efter en form som heter rektangel, med form-ID 1, och ställer in fyllningsbakgrunds- och förgrundsfärgerna.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetFillData-SetFillData.cs" >}}
### **Hämta ärvd fyllningsdata för en Visio-form**
 Visio-formerna kan ärva den överordnade stilen och huvudformen. Utvecklare kan hämta eller ställa in ärvd fyllningsdata för en Visio-form. Egenskapen InheritFill, exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass, innehåller fyllningsformateringsvärdena för formen som ärvs av den överordnade stilen och huvudformen.
#### **Hämta ärvt fyllningsdataprogrammeringsexempel**
Följande kodavsnitt hämtar formens ärvda fyllningsdata. Kontrollera denna exempelkod:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RetrieveInheritedFillData-RetrieveInheritedFillData.cs" >}}
