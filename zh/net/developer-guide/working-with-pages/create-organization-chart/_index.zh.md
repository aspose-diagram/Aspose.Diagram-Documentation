---
title: 创建组织结构图
type: docs
weight: 100
url: /zh/net/create-organization-chart/
description: 本节介绍如何使用 Aspose.Diagram 创建组织结构图。
---
## **创建组织结构图**
本节介绍如何使用 Aspose.Diagram 创建组织结构图。
### **创建一个 CompactTree 风格的组织结构图**
的布局方法[页](http://www.aspose.com/api/net/diagram/aspose.diagram/page)类自动将页面中的形状和连接器布局为 CompactTree 样式的组织结构图。

下面的代码显示了如何：

1. 从模板创建一个 diagram。
1. 将组织节点形状添加到页面。
1. 将连接器添加到页面以连接形状及其父级。
1. 通过调用 Layout 方法自动布局
1. 保存 diagram
#### **创建一个 CompactTree 风格的组织结构图编程示例**
使用以下代码使用 Aspose.Diagram 创建 CompactTree 样式组织结构图。


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_CompactTreeChart();

// Load masters from any existing diagram, stencil or template
// And add in the new diagram
string visioStencil = dataDir + "Basic Shapes.vss";
const string rectangleMaster = "Rectangle";
const string connectorMaster = "Dynamic connector";
const int pageNumber = 0;
const double width = 1;
const double height = 1;
double pinX = 4.25;
double pinY = 9.5;
// Define values to construct the hierarchy
List<string> listPos = new List<string>(new string[] { "0", "0:0", "0:1", "0:2", "0:3", "0:4", "0:5", "0:6", "0:0:0", "0:0:1", "0:3:0", "0:3:1", "0:3:2", "0:6:0", "0:6:1" });
// Define a Hashtable to map the string name to long shape id
Hashtable shapeIdMap = new Hashtable();
// Create a new diagram
Diagram diagram = new Diagram(visioStencil);
diagram.Pages[pageNumber].PageSheet.PageProps.PageWidth.Value = 11;
foreach (string orgnode in listPos)
{
    // Add a new rectangle shape
    long rectangleId = diagram.AddShape(pinX++, pinY++, width, height, rectangleMaster, pageNumber);
    // Set the new shape's properties
    Shape shape = diagram.Pages[pageNumber].Shapes.GetShape(rectangleId);
    shape.Text.Value.Add(new Txt(orgnode));
    shape.Name = orgnode;
    shapeIdMap.Add(orgnode, rectangleId);
}
// Create connections between nodes
foreach (string orgName in listPos)
{
    int lastColon = orgName.LastIndexOf(':');
    if(lastColon > 0)
    {
        string parendName = orgName.Substring(0, lastColon);
        long shapeId = (long)shapeIdMap[orgName];
        long parentId = (long)shapeIdMap[parendName];
        Shape connector1 = new Shape();
        long connecter1Id = diagram.AddShape(connector1, connectorMaster, pageNumber);
        diagram.Pages[pageNumber].ConnectShapesViaConnector(parentId, ConnectionPointPlace.Right,
            shapeId, ConnectionPointPlace.Left, connecter1Id);
    }
}

//auto layout CompactTree chart
LayoutOptions compactTreeOptions = new LayoutOptions
{
    LayoutStyle = LayoutStyle.CompactTree,
    Direction = LayoutDirection.DownThenRight,
    EnlargePage = false
};

diagram.Pages[pageNumber].Layout(compactTreeOptions);

// Save diagram
diagram.Save(dataDir + "CompactTreeChart_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


|**结果**|
|:- |
|![CompactTreeChart_out.vsdx](CompactTreeChart.png)|

### **创建流程图样式的组织结构图**
的布局方法[页](http://www.aspose.com/api/net/diagram/aspose.diagram/page)类自动将页面中的形状和连接器布局为流程图样式的组织结构图。

下面的代码显示了如何：

1. 从模板创建一个 diagram。
1. 将组织节点形状添加到页面。
1. 将连接器添加到页面以连接形状及其父级。
1. 通过调用 Layout 方法自动布局
1. 保存 diagram
#### **创建流程图样式的组织结构图编程示例**
使用以下代码使用 Aspose.Diagram 创建流程图样式组织结构图。


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_FlowChart();

// Load masters from any existing diagram, stencil or template
// And add in the new diagram
string visioStencil = dataDir + "Basic Shapes.vss";
const string rectangleMaster = "Rectangle";
const string connectorMaster = "Dynamic connector";
const int pageNumber = 0;
const double width = 1;
const double height = 1;
double pinX = 4.25;
double pinY = 9.5;
// Define values to construct the hierarchy
List<string> listPos = new List<string>(new string[] { "0", "0:0", "0:1", "0:2", "0:3", "0:4", "0:5", "0:6", "0:0:0", "0:0:1", "0:3:0", "0:3:1", "0:3:2", "0:6:0", "0:6:1" });
// Define a Hashtable to map the string name to long shape id
Hashtable shapeIdMap = new Hashtable();
// Create a new diagram
Diagram diagram = new Diagram(visioStencil);
foreach (string orgnode in listPos)
{
    // Add a new rectangle shape
    long rectangleId = diagram.AddShape(pinX++, pinY++, width, height, rectangleMaster, pageNumber);
    // Set the new shape's properties
    Shape shape = diagram.Pages[pageNumber].Shapes.GetShape(rectangleId);
    shape.Text.Value.Add(new Txt(orgnode));
    shape.Name = orgnode;
    shapeIdMap.Add(orgnode, rectangleId);
}
// Create connections between nodes
foreach (string orgName in listPos)
{
    int lastColon = orgName.LastIndexOf(':');
    if(lastColon > 0)
    {
        string parendName = orgName.Substring(0, lastColon);
        long shapeId = (long)shapeIdMap[orgName];
        long parentId = (long)shapeIdMap[parendName];
        Shape connector1 = new Shape();
        long connecter1Id = diagram.AddShape(connector1, connectorMaster, pageNumber);
        diagram.Pages[pageNumber].ConnectShapesViaConnector(parentId, ConnectionPointPlace.Right,
            shapeId, ConnectionPointPlace.Left, connecter1Id);
    }
}

//auto layout FlowChart
LayoutOptions flowChartOptions = new LayoutOptions
{
    LayoutStyle = LayoutStyle.FlowChart,
    Direction = LayoutDirection.TopToBottom,
    EnlargePage = true
};

diagram.Pages[pageNumber].Layout(flowChartOptions);

// Save diagram
diagram.Save(dataDir + "FlowChart_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


|**结果**|
|:- |
|![FlowChart_out.vsdx](FlowChart.png)|
