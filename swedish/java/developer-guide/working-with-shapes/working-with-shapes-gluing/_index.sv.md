---
title: Arbeta med formlimning
type: docs
weight: 10
url: /sv/java/working-with-shapes-gluing/
---
## **Få kontakterna limmade till en speciell form**
[Lägg till och anslut Visio Former](/diagram/sv/java/add-and-connect-visio-shapes/) förklarar hur man lägger till en form och kopplar den till andra former i Microsoft Visio diagram med Aspose.Diagram for Java. Det är också möjligt att hitta kopplingar som är limmade på denna form.
### **Att få limmade former**
 GluedShapes-metoden exponerad av[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)klass kan användas för att få en lista över ID:n för alla kopplingar som är limmade på en form, eller, om formen i fråga är en koppling, ID:n för de former den är ansluten till. GetShape-metoden, exponerad av[ShapeCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) klass, kan sedan användas för att hitta en form med dess ID.

Koden nedan visar hur man:

1. Ladda en exempelfil.
1. Få tillgång till en viss form.
1. Få en lista med ID:n för alla kontakter som är limmade på den här formen.
#### **Få kopplingar limmade Programmeringsprov**
Använd följande kod i din Java-applikation för att hitta alla kontakter som är limmade på en form med Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-Glue-GetGluedConnectors-GetGluedConnectors.java" >}}
## **Limma Visio Former tillsammans med anslutningspunkt**
Aspose.Diagram for Java låter utvecklare limma ihop former genom anslutningspunkterna.
### **Limformer**
 GlueShapes-metoden exponerad av[Sida](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) klass kan användas.

|<p>**Ingång diagram** </p><p>![todo:image_alt_text](http://i.imgur.com/Z69f4hg.png)</p>|<p>**Den diagram efter limning av formerna** </p><p>![todo:image_alt_text](http://i.imgur.com/5TJpDwc.png)</p>|
|:- |:- |
Koden nedan visar hur man:

1. Ladda en exempelfil.
1. Limma former.
1. Spara diagram.
#### **Lim Visio Formprogrammeringsprov**
Använd följande kod i din Java-applikation för att limma former genom anslutningspunkterna:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-Glue-GlueVisioShapes-GlueVisioShapes.java" >}}
## **Limma former inuti behållaren**
Aspose.Diagram for Java gör det möjligt för utvecklare att limma gruppformer inuti en behållare.
### **Limgruppsform**
Metoden GlueShapesInContainer som exponeras av klassen Page kan användas.

|<p>**Ingång diagram** </p><p>![todo:image_alt_text](http://i.imgur.com/HRRzIEh.png)</p>|<p>**Den diagram efter limning av gruppformerna** </p><p>![todo:image_alt_text](http://i.imgur.com/YxCiOgU.png)</p>|
|:- |:- |
Koden nedan visar hur man:

1. Ladda en exempelfil.
1. Limma gruppformer.
1. Spara diagram.
#### **Limformer inuti programmeringsprov**
Använd följande kod i din Java-applikation för att limma gruppform inuti en behållare:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-Glue-GlueContainerShape-GlueContainerShape.java" >}}
