---
title: Crear organigrama
type: docs
weight: 100
url: /es/java/create-organization-chart/
description: Esta sección explica cómo crear un organigrama usando Aspose.Diagram for Java.
---
## ** Crear un organigrama**
Esta sección explica cómo crear un organigrama usando Aspose.Diagram for Java.
### **Crear un organigrama de estilo CompactTree**
 El método de diseño de la[Página](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)clase de diseño automático de las formas y conectores en la página como un organigrama de estilo CompactTree.

El siguiente código muestra cómo:

1. Cree un diagram a partir de la plantilla.
1. Agregue formas de nodos de organización a la página.
1. Agregue conectores a la página para conectar la forma y su padre.
1. Diseño automático invocando el método de diseño
1. guardar diagram
#### **Cree un ejemplo de programación de organigrama de estilo CompactTree**
Use el siguiente código para crear un organigrama de estilo CompactTree usando Aspose.Diagram for Java.


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


|**Resultado**|
|:- |
|![CompactTreeChart_out.vsdx](CompactTreeChart.png)|

### **Crear un organigrama de estilo FlowChart**
 El método de diseño de la[Página](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) clase de diseño automático de las formas y conectores en la página como un organigrama de estilo FlowChart.

El siguiente código muestra cómo:

1. Cree un diagram a partir de la plantilla.
1. Agregue formas de nodos de organización a la página.
1. Agregue conectores a la página para conectar la forma y su padre.
1. Diseño automático invocando el método de diseño
1. guardar diagram
#### **Cree un ejemplo de programación de organigrama de estilo FlowChart**
Use el siguiente código para crear un organigrama de estilo FlowChart usando Aspose.Diagram for Java.


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


|**Resultado**|
|:- |
|![Diagrama de flujo_out.vsdx](FlowChart.png)|
