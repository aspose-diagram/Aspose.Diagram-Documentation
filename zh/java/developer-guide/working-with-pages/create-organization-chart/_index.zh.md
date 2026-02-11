---
title: 创建组织结构图
type: docs
weight: 100
url: /zh/java/create-organization-chart/
description: 本节介绍如何使用 Aspose.Diagram for Java 创建组织结构图。
---
## **创建组织结构图**
本节介绍如何使用 Aspose.Diagram for Java 创建组织结构图。
### **创建一个 CompactTree 风格的组织结构图**
的布局方法[页](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)类自动将页面中的形状和连接器布局为 CompactTree 样式的组织结构图。

下面的代码显示了如何：

1. 从模板创建一个 diagram。
1. 将组织节点形状添加到页面。
1. 将连接器添加到页面以连接形状及其父级。
1. 通过调用 Layout 方法自动布局
1. 保存 diagram
#### **创建一个 CompactTree 风格的组织结构图编程示例**
使用以下代码使用 Aspose.Diagram for Java 创建 CompactTree 样式组织结构图。

```
{{< highlight "java" >}}
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
```

|**结果**|
|:- |
|![CompactTreeChart_out.vsdx](CompactTreeChart.png)|

### **创建流程图样式的组织结构图**
的布局方法[页](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)类自动将页面中的形状和连接器布局为流程图样式的组织结构图。

下面的代码显示了如何：

1. 从模板创建一个 diagram。
1. 将组织节点形状添加到页面。
1. 将连接器添加到页面以连接形状及其父级。
1. 通过调用 Layout 方法自动布局
1. 保存 diagram
#### **创建流程图样式的组织结构图编程示例**
使用以下代码使用 Aspose.Diagram for Java 创建流程图样式组织结构图。

```
{{< highlight "java" >}}
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
```

|**结果**|
|:- |
|![FlowChart_out.vsdx](FlowChart.png)|
