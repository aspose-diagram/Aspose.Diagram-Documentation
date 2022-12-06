---
title: Ställ in Visio Shapes XForm, Line och Fill Data
type: docs
weight: 70
url: /sv/java/set-visio-shape-s-xform-line-and-fill-data/
---
## **Ställa in XForm-data**
 XForm-elementet är en del av XML-schemat Microsoft Visio. XForm anger en forms position, till exempel bredd, höjd, rotation och om formen har vänts. De[XForm](https://reference.aspose.com/diagram/java/com.aspose.diagram/xform) egendom, exponerad av[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) klass, stöder objektet Aspose.Diagram.XForm. XForm-egenskapen kan användas för att hämta eller uppdatera en forms XForm-data. Kodexemplen i den här artikeln ändrar PinX (X-koordinat) och PinY (Y-koordinat) XForm-värden för att flytta formerna på sidan.

**Ingång diagram** 

![todo:image_alt_text](set-visio-shape-s-xform-line-and-fill-data_1.png)

**diagram efter den** **PinX** **och** **PinY** **värden har ändrats** 

![todo:image_alt_text](set-visio-shape-s-xform-line-and-fill-data_2.png)

Processen för att uppdatera XForm-data är:

1. Ladda en diagram.# Hitta en viss form.# Uppdatera formens XForm-data.
1. Spara diagram.
### **Programmeringsexempel**
Kodavsnittet nedan visar hur du uppdaterar en forms XForm-data. Koden letar efter en process för formnamn, med form-ID 1, och ställer in dess X- och Y-koordinater till 5.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SetXFormdata-SetXFormdata.java" >}}
## **Ställ in Visio Shape's Line Data**
Former kan formateras på flera sätt. Den här artikeln visar hur du anger en linjes attribut.

Microsoft Visio låter användare formatera linjer på olika sätt. Aspose.Diagram for Java stöder:

- Vikt: en linjes tjocklek.
- Färg: ställ in formens linjefärg.
- Linjefärgstransparens: ställ in formens linjefärgtransparens i procent.
- Mönster: definierar om linjen är heldragen, streckad eller har ett annat mönster.
- Avrundning: radien på hörnen.
- Start- och slutpilar: ange om linjen har pilar.
- Början och slutet pilstorlekar: ställ in pilstorlekarna.
- Cap: avrundningen av linjen slutar.
### **Ändra linjefärg, vikt, strecktyp, transparens, avrundning, piltyp och pilstorlek för en forms kant**
 De[Linje](https://reference.aspose.com/diagram/java/com.aspose.diagram/line) egendom, exponerad av[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)klass, stöder objektet Aspose.Diagram.Line. Den här egenskapen kan användas för att hämta eller uppdatera en forms linjedata.
#### **Linjedataprogrammeringsexempel**
Följande kodbit uppdaterar formens linjedata.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SetLineData-SetLineData.java" >}}
## **Ställ in Visio Shape's Fill Data**
Former kan formateras på flera sätt. Det här avsnittet beskriver hur du anger en forms fyllning.

 Microsoft Office Visio låter användare formatera fyllningar på olika sätt. De[Fylla](https://reference.aspose.com/diagram/java/com.aspose.diagram/fill) klass av Aspose.Diagram for Java API stöder inställning:

- Bakgrunds- och förgrundsfärger.
- Genomskinlighet.
- Fyllningsmönster.
- Skuggor.
### **Ställa in fyllningsvärden**
Fill-egenskapen, exponerad av Shape-klassen, stöder objektet Aspose.Diagram.Fill. Fill-egenskapen kan användas för att hämta eller uppdatera en forms fyllningsdata.

|<p>**Ingången diagram** </p><p>![todo:image_alt_text](http://i.imgur.com/OrhEecb.png)</p>|<p>**diagram efter att ha ändrat fyllningsfärgen** </p><p>![todo:image_alt_text](http://i.imgur.com/HO0wmZ8.png)</p>|
|:- |:- |
#### **Fyll i dataprogrammeringsexempel**
Följande kodavsnitt uppdaterar en forms fyllningsdata. Koden letar efter en form som heter rektangel, med form-ID 1, och ställer in fyllningsbakgrunds- och förgrundsfärgerna.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SetFillData-SetFillData.java" >}}
### **Hämta ärvd fyllningsdata för en Visio-form**
Visio-formerna kan ärva den överordnade stilen och huvudformen. Utvecklare kan hämta eller ställa in ärvd fyllningsdata för en Visio-form. Egenskapen InheritFill, exponerad av Shape-klassen, innehåller fyllningsformateringsvärdena för formen som ärver av den överordnade stilen och masterformen.
#### **Hämta ärvt fyllningsdataprogrammeringsexempel**
Följande kodavsnitt hämtar formens ärvda fyllningsdata. Kontrollera denna exempelkod:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveInheritedFillData-RetrieveInheritedFillData.java" >}}
