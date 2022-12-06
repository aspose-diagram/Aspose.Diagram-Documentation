---
title: Arbeta med formlimning
type: docs
weight: 40
url: /sv/net/working-with-shapes-gluing/
description: Det här avsnittet förklarar hur man får former som limmas till en viss form med Aspose.Diagram.
---
## **Få kontakterna limmade till en speciell form**
[Lägg till och anslut Visio Former](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/) förklarar hur man lägger till en form och kopplar den till andra former i Microsoft Visio diagram med Aspose.Diagram for .NET. Det är också möjligt att hitta kopplingar som är limmade på denna form.
### **Att få limmade former**
 GluedShapes-metoden exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)klass kan användas för att få en lista över ID:n för alla kopplingar som är limmade på en form, eller, om formen i fråga är en koppling, ID:n för de former den är ansluten till. GetShape-metoden, exponerad av[ShapeCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/shapecollection) klass, kan sedan användas för att hitta en form med dess ID.

Koden nedan visar hur man:

1. Ladda en exempelfil.
1. Få tillgång till en viss form.
1. Få en lista med ID:n för alla kontakter som är limmade på den här formen.
#### **Få kopplingar limmade Programmeringsprov**
Använd följande kod i din .NET-applikation för att hitta alla kontakter som är limmade på en form med Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Shapes-Gluing-GetGluedConnectors-GetGluedConnectors.cs" >}}
## **Limma Visio Former tillsammans med anslutningspunkt**
Aspose.Diagram for .NET låter utvecklare limma ihop former genom anslutningspunkterna.
### **Limformer**
 GlueShapes-metoden exponerad av[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page) klass kan användas.

|<p>**Ingång diagram** </p><p>![todo:image_alt_text](working-with-shapes-gluing_1.png)</p>|<p>**Den diagram efter limning av formerna** </p><p>![todo:image_alt_text](working-with-shapes-gluing_2.png)</p>|
|:- |:- |
Koden nedan visar hur man:

1. Ladda en exempelfil.
1. Limma former.
1. Spara diagram.
#### **Lim Visio Formprogrammeringsprov**
Använd följande kod i din .NET-applikation för att limma former genom anslutningspunkterna:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Shapes-Gluing-GlueVisioShapes-GlueVisioShapes.cs" >}}
## **Limma former inuti behållaren**
Aspose.Diagram for .NET gör det möjligt för utvecklare att limma gruppformer inuti en behållare.
### **Limgruppsform**
 GlueShapesInContainer-metoden exponerad av[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page) klass kan användas.

|<p>**Ingång diagram** </p><p>![todo:image_alt_text](working-with-shapes-gluing_3.png)</p>|<p>**Den diagram efter limning av gruppformerna** </p><p>![todo:image_alt_text](working-with-shapes-gluing_4.png)</p>|
|:- |:- |
Koden nedan visar hur man:

1. Ladda en exempelfil.
1. Limma gruppformer.
1. Spara diagram.
#### **Limformer inuti programmeringsprov**
Använd följande kod i din .NET-applikation för att limma gruppform inuti en behållare:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Shapes-Gluing-GlueContainerShape-GlueContainerShape.cs" >}}
