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


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetGluedConnectors.class);   
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "RetrieveShapeInfo.vsd");
// get shape by an ID
Shape shape = diagram.getPages().get(0).getShapes().getShape(90);
// get all glued 1D shapes
long[] gluedShapeIds = shape.gluedShapes(GluedShapesFlags.GLUED_SHAPES_ALL_1_D, null, null);

// display shape ID and name
for (long id : gluedShapeIds)
{
    shape = diagram.getPages().get(0).getShapes().getShape(id);
    System.out.println("ID: " + shape.getID() + "\t\t Name: " + shape.getName());
}

{{< /highlight >}}

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


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GlueVisioShapes.class);
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.getPages().getPage("Page-1");
// set shape id
long shape1_ID = 7;
long shape2_ID = 494;
// Glue shapes
page.glueShapes(shape1_ID, ConnectionPointPlace.CENTER, shape2_ID);

// Save diagram
diagram.save(dataDir + "GlueVisioShapes_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

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


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GlueContainerShape.class);   
// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get a particular page
Page page = diagram.getPages().getPage("Page-1");

// The ID of shape which is glue from Aspose.Diagram.Shape.
long shapeFromId = 779;
// The location on the first connection index where to glue
int shapeToBeginConnectionIndex = 72;
// The location on the end connection index where to glue
int shapeToEndConnectionIndex = 73;
// The ID of shape where to glue to Aspose.Diagram.Shape.
long shapeToId = 743;

// Glue shapes in container
page.glueShapesInContainer(shapeFromId, shapeToBeginConnectionIndex, shapeToEndConnectionIndex, shapeToId);

// Glue shapes in container using connection name
// page.GlueShapesInContainer(fasId, "U05L", "U05R", cabinetId1);

// Save diagram
diagram.save(dataDir + "GlueContainerShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

