---
title: Rotera, ändra position och anslut delformer
type: docs
weight: 60
url: /sv/java/rotate-change-the-position-and-connect-sub-shapes/
---
## **Rotera en form med lämplig vinkel**
 Aspose.Diagram for Java låter dig rotera en form till vilken vinkel som helst. SetAngle-metoden exponerad av[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) klass kan användas för att rotera en form till valfri vinkel. Det tar en enda parameter som en vinkel.
### **Rotera ett formprogrammeringsprov**
Använd följande kod i din Java-applikation för att rotera en form med Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RotateVisioShape-RotateVisioShape.java" >}}
## **Ändra positionen för en form**
Formklassen låter dig ändra positionen för en form. Anslutningslinjen justeras automatiskt när formen flyttas till en annan position.

Metoderna Move och MoveTo, exponerade av Shape-klassen, stöder att ändra positionen för en form som en del av en grupp eller inte.
Kodexemplen i den här artikeln flyttar en form på sidan.
**Ingång diagram** 

![todo:image_alt_text](http://i.imgur.com/cThgWnB.png)


**diagram efter att formen har flyttats** 

![todo:image_alt_text](http://i.imgur.com/Q3QByqe.png)

Processen för att flytta en form är:

1. Ladda ett diagram.
1. Hitta en viss form.
1. Flytta formen till en annan plats
1. Spara diagram.
### **Ändra positionsprogrammeringsexempel**
Kodavsnittet nedan visar hur du flyttar formen. Koden hämtar en Visio-sida med namn och form med ID 16 och flyttar dess position.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-MoveVisioShape-MoveVisioShape.java" >}}
## **Anslut underformer av grupperna**
Det här ämnet utvecklar hur man kopplar samman två underformer av två olika gruppformer i Microsoft Visio diagram med Aspose.Diagram for Java.

 ConnectShapesViaConnector-metoden exponerad av[Sida](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) klass kan användas för att koppla ihop formerna med deras ID. AddShape-metoden, exponerad av[Diagram](https://reference.aspose.com/diagram/java)klass, kan användas för att lägga till en form.

|<p>**Ingången diagram** </p><p>![todo:image_alt_text](http://i.imgur.com/74rDby5.png)</p>|<p>**Den diagram efter anslutning av sub-former** </p><p>![todo:image_alt_text](http://i.imgur.com/c387dZJ.png)</p>|
|:- |:- |
Koden nedan visar hur man:

1. Ladda en exempelfil.
1. Gå till en viss sida.
1. Lägg till en dynamisk kopplingsform på den valda sidan.
1. Anslut underformer
### **Connect Sub-shapes programmeringsexempel**
Använd följande kod i din Java-applikation för att ansluta underformerna till två olika gruppformer med Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ConnectVisioSubShapes-ConnectVisioSubShapes.java" >}}
## **Få formerna kopplade till en viss form**
[Lägg till och anslut Visio Former](/diagram/sv/java/add-and-connect-visio-shapes/) förklarar hur man lägger till en form och kopplar den till andra former i Microsoft Visio diagram med Aspose.Diagram for Java. Det är också möjligt att hitta former som är kopplade till en specifik form.

 ConnectedShapes-metoden exponerad av[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) klass kan användas för att få ID:n för formerna kopplade till en form. GetShape-metoden, exponerad av[ShapeCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) klass, kan sedan användas för att hitta en form med dess ID.

Koden nedan visar hur man:

1. Ladda en exempelfil.
1. Få tillgång till en viss form.
1. Hämta namnen på alla former som är kopplade till den valda formen.
### **Få formprogrammeringsexempel**
Använd följande kod i din Java-applikation för att hitta alla former som är kopplade till en specifik form med Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-GetAllConnectedShapes-GetAllConnectedShapes.java" >}}
