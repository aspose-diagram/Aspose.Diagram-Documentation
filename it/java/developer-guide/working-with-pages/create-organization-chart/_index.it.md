---
title: Crea organigramma
type: docs
weight: 100
url: /it/java/create-organization-chart/
description: Questa sezione spiega come creare un organigramma utilizzando Aspose.Diagram for Java.
---
## ** Crea un organigramma**
Questa sezione spiega come creare un organigramma utilizzando Aspose.Diagram for Java.
### **Creare un organigramma in stile CompactTree**
 Il metodo di layout del[Pagina](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)class layout automatico delle forme e dei connettori nella pagina come organigramma in stile CompactTree.

Il codice seguente mostra come:

1. Crea uno diagram dallo stencil.
1. Aggiungi le forme dei nodi dell'organizzazione alla pagina.
1. Aggiungi connettori alla pagina per connettere la forma e il suo genitore.
1. Layout automatico richiamando Layout mothod
1. salvo diagram
#### **Creare un esempio di programmazione di organigrammi in stile CompactTree**
Utilizzare il codice seguente per creare un organigramma in stile CompactTree utilizzando Aspose.Diagram for Java.


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


|**Risultato**|
|:- |
|![CompactTreeChart_out.vsdx](CompactTreeChart.png)|

### **Creare un organigramma in stile diagramma di flusso**
 Il metodo di layout del[Pagina](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) class layout automatico delle forme e dei connettori nella pagina come un organigramma in stile diagramma di flusso.

Il codice seguente mostra come:

1. Crea uno diagram dallo stencil.
1. Aggiungi le forme dei nodi dell'organizzazione alla pagina.
1. Aggiungi connettori alla pagina per connettere la forma e il suo genitore.
1. Layout automatico richiamando Layout mothod
1. salvo diagram
#### **Creare un esempio di programmazione di organigramma in stile diagramma di flusso**
Utilizzare il codice seguente per creare un organigramma in stile diagramma di flusso utilizzando Aspose.Diagram for Java.


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


|**Risultato**|
|:- |
|![Diagramma di flusso_out.vsdx](FlowChart.png)|
