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

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RotateVisioShape.class); 
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");
// get shape by id
Shape shape = page.getShapes().getShape(16);

// Add a shape and set the angle
shape.setAngle(190);

// Save diagram
diagram.save(dataDir + "RotateVisioShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
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

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(MoveVisioShape.class);  
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");
// get shape by id
Shape shape = page.getShapes().getShape(16);
// move shape from its position, it adds values in coordinates
shape.move(1, 1);

// save diagram
diagram.save(dataDir + "MoveVisioShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
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

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ConnectVisioSubShapes.class);   
// set sub shape ids
long shapeFromId = 2;
long shapeToId = 4;

// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// access a particular page
Page page = diagram.getPages().getPage("Page-3");
       
// initialize connector shape
Shape shape = new Shape();
shape.getLine().getEndArrow().setValue(4);
shape.getLine().getLineWeight().setValue(0.01388);

// add shape
long connecter1Id = diagram.addShape(shape, "Dynamic connector", page.getID());
// connect sub-shapes
page.connectShapesViaConnector(shapeFromId, ConnectionPointPlace.RIGHT, shapeToId, ConnectionPointPlace.LEFT, connecter1Id);
// save Visio drawing
diagram.save(dataDir + "ConnectVisioSubShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Få formerna kopplade till en viss form**
[Lägg till och anslut Visio Former](/diagram/sv/java/add-and-connect-visio-shapes/) förklarar hur man lägger till en form och kopplar den till andra former i Microsoft Visio diagram med Aspose.Diagram for Java. Det är också möjligt att hitta former som är kopplade till en specifik form.

 ConnectedShapes-metoden exponerad av[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) klass kan användas för att få ID:n för formerna kopplade till en form. GetShape-metoden, exponerad av[ShapeCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shapecollection) klass, kan sedan användas för att hitta en form med dess ID.

Koden nedan visar hur man:

1. Ladda en exempelfil.
1. Få tillgång till en viss form.
1. Hämta namnen på alla former som är kopplade till den valda formen.
### **Få formprogrammeringsexempel**
Använd följande kod i din Java-applikation för att hitta alla former som är kopplade till en specifik form med Aspose.Diagram for Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetAllConnectedShapes.class);
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get shape by id
Shape shape = diagram.getPages().getPage("Page-3").getShapes().getShape(16);
// get connected shapes
long[] connectedShapeIds = shape.connectedShapes(ConnectedShapesFlags.CONNECTED_SHAPES_ALL_NODES, null);

for (long id : connectedShapeIds)
{
    shape = diagram.getPages().getPage("Page-3").getShapes().getShape(id);
    System.out.println("ID: " + shape.getID() + "\t\t Name: " + shape.getName());
}

{{< /highlight >}}
```
