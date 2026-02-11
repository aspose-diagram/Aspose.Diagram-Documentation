---
title: Organigramm erstellen
type: docs
weight: 100
url: /de/java/create-organization-chart/
description: In diesem Abschnitt wird erläutert, wie Sie mit Aspose.Diagram for Java ein Organigramm erstellen.
---
## ** Erstellen Sie ein Organigramm**
In diesem Abschnitt wird erläutert, wie Sie mit Aspose.Diagram for Java ein Organigramm erstellen.
### **Erstellen Sie ein Organigramm im CompactTree-Stil**
 Die Layout-Methode der[Buchseite](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)-Klasse ordnet die Shapes und Konnektoren auf der Seite automatisch als Organigramm im CompactTree-Stil an.

Der folgende Code zeigt, wie man:

1. Erstellen Sie eine diagram aus der Schablone.
1. Organisationsknoten-Shapes zur Seite hinzufügen.
1. Fügen Sie der Seite Verbinder hinzu, um die Form und ihr übergeordnetes Element zu verbinden.
1. Automatisches Layout durch Aufrufen der Layout-Methode
1. außer diagram
#### **Erstellen Sie ein Programmierbeispiel für ein Organigramm im CompactTree-Stil**
Verwenden Sie den folgenden Code, um ein Organigramm im CompactTree-Stil mit Aspose.Diagram for Java zu erstellen.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DrawCompactTreeChart.class);

// Load masters from any existing diagram, stencil or template
// And add in the new diagram
String visioStencil = dataDir + "Basic Shapes.vss";
String rectangleMaster = "Rectangle";
String connectorMaster = "Dynamic connector";
int pageNumber = 0;
double width = 1;
double height = 1;
double pinX = 4.25;
double pinY = 9.5;
// Define values to construct the hierarchy
List<String> listPos = Arrays.asList(new String[] { "0", "0:0", "0:1", "0:2", "0:3", "0:4", "0:5", "0:6", "0:0:0", "0:0:1", "0:3:0", "0:3:1", "0:3:2", "0:6:0", "0:6:1" });
// Define a Hashtable to map the string name to long shape id
Hashtable shapeIdMap = new Hashtable();
// Create a new diagram
Diagram diagram = new Diagram(visioStencil);
diagram.getPages().get(pageNumber).getPageSheet().getPageProps().getPageWidth().setValue(11);
for (String orgnode : listPos)
{
    // Add a new rectangle shape
    long rectangleId = diagram.addShape(pinX++, pinY++, width, height, rectangleMaster, pageNumber);
    // Set the new shape's properties
    Shape shape = diagram.getPages().get(pageNumber).getShapes().getShape(rectangleId);
    shape.getText().getValue().add(new Txt(orgnode));
    shape.setName(orgnode);
    shapeIdMap.put(orgnode, rectangleId);
}
// Create connections between nodes
for (String orgName : listPos)
{
    int lastColon = orgName.lastIndexOf(':');
    if(lastColon > 0)
    {
        String parendName = orgName.substring(0, lastColon);
        long shapeId = (long)shapeIdMap.get(orgName);
        long parentId = (long)shapeIdMap.get(parendName);
        Shape connector1 = new Shape();
        long connecter1Id = diagram.addShape(connector1, connectorMaster, pageNumber);
        diagram.getPages().get(pageNumber).connectShapesViaConnector(parentId, ConnectionPointPlace.RIGHT,
            shapeId, ConnectionPointPlace.LEFT, connecter1Id);
    }
}

//auto layout CompactTree chart
LayoutOptions compactTreeOptions = new LayoutOptions();
compactTreeOptions.setLayoutStyle(LayoutStyle.COMPACT_TREE);
compactTreeOptions.setDirection(LayoutDirection.DOWN_THEN_RIGHT);
compactTreeOptions.setEnlargePage(false);

diagram.getPages().get(pageNumber).layout(compactTreeOptions);

// Save diagram
diagram.save(dataDir + "DrawCompactTreeChart_java.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


|**Ergebnis**|
|:- |
|![CompactTreeChart_out.vsdx](CompactTreeChart.png)|

### **Erstellen Sie ein Organigramm im Stil eines Flussdiagramms**
 Die Layout-Methode der[Buchseite](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) Klasse ordnet die Formen und Konnektoren auf der Seite automatisch als Organigramm im Stil eines Flussdiagramms an.

Der folgende Code zeigt, wie man:

1. Erstellen Sie eine diagram aus der Schablone.
1. Organisationsknoten-Shapes zur Seite hinzufügen.
1. Fügen Sie der Seite Verbinder hinzu, um die Form und ihr übergeordnetes Element zu verbinden.
1. Automatisches Layout durch Aufrufen der Layout-Methode
1. außer diagram
#### **Erstellen Sie ein Programmierbeispiel für ein Organigramm im Stil eines Flussdiagramms**
Verwenden Sie den folgenden Code, um ein Organigramm im Flussdiagrammstil mit Aspose.Diagram for Java zu erstellen.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DrawFlowChart.class);

// Load masters from any existing diagram, stencil or template
// And add in the new diagram
String visioStencil = dataDir + "Basic Shapes.vss";
String rectangleMaster = "Rectangle";
String connectorMaster = "Dynamic connector";
int pageNumber = 0;
double width = 1;
double height = 1;
double pinX = 4.25;
double pinY = 9.5;
// Define values to construct the hierarchy
List<String> listPos = Arrays.asList(new String[] { "0", "0:0", "0:1", "0:2", "0:3", "0:4", "0:5", "0:6", "0:0:0", "0:0:1", "0:3:0", "0:3:1", "0:3:2", "0:6:0", "0:6:1" });
// Define a Hashtable to map the string name to long shape id
Hashtable shapeIdMap = new Hashtable();
// Create a new diagram
Diagram diagram = new Diagram(visioStencil);
diagram.getPages().get(pageNumber).getPageSheet().getPageProps().getPageWidth().setValue(11);
for (String orgnode : listPos)
{
    // Add a new rectangle shape
    long rectangleId = diagram.addShape(pinX++, pinY++, width, height, rectangleMaster, pageNumber);
    // Set the new shape's properties
    Shape shape = diagram.getPages().get(pageNumber).getShapes().getShape(rectangleId);
    shape.getText().getValue().add(new Txt(orgnode));
    shape.setName(orgnode);
    shapeIdMap.put(orgnode, rectangleId);
}
// Create connections between nodes
for (String orgName : listPos)
{
    int lastColon = orgName.lastIndexOf(':');
    if(lastColon > 0)
    {
        String parendName = orgName.substring(0, lastColon);
        long shapeId = (long)shapeIdMap.get(orgName);
        long parentId = (long)shapeIdMap.get(parendName);
        Shape connector1 = new Shape();
        long connecter1Id = diagram.addShape(connector1, connectorMaster, pageNumber);
        diagram.getPages().get(pageNumber).connectShapesViaConnector(parentId, ConnectionPointPlace.RIGHT,
            shapeId, ConnectionPointPlace.LEFT, connecter1Id);
    }
}

//auto layout FlowChart
LayoutOptions flowChartOptions = new LayoutOptions();
flowChartOptions.setLayoutStyle(LayoutStyle.FLOW_CHART);
flowChartOptions.setDirection(LayoutDirection.TOP_TO_BOTTOM);
flowChartOptions.setEnlargePage(true);

diagram.getPages().get(pageNumber).layout(flowChartOptions);

// Save diagram
diagram.save(dataDir + "DrawFlowChart_java.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


|**Ergebnis**|
|:- |
|![FlowChart_out.vsdx](FlowChart.png)|
