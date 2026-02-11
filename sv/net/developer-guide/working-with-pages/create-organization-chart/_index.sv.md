---
title: Skapa organisationsschema
type: docs
weight: 100
url: /sv/net/create-organization-chart/
description: Det här avsnittet förklarar hur du skapar ett organisationsschema med Aspose.Diagram.
---
## ** Skapa ett organisationsschema**
Det här avsnittet förklarar hur du skapar ett organisationsschema med Aspose.Diagram.
### **Skapa ett organisationsschema i CompactTree-stil**
 Layoutmetoden för[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page) klass autolayout formerna och kopplingarna på sidan som ett organisationsdiagram i CompactTree-stil.

Koden nedan visar hur man:

1. Skapa ett diagram från stencil.
1. Lägg till organisationsnodformer på sidan.
1. Lägg till kopplingar till sidan för att koppla samman form och dess överordnade.
1. Automatisk layout genom att åberopa layoutmetoden
1. spara diagram
#### **Skapa ett CompactTree-stil Organisationsschema programmeringsexempel**
Använd följande kod för att skapa ett CompactTree-organisationsschema med Aspose.Diagram.

```
{{< highlight "csharp" >}}
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
```

|**Resultat**|
|:- |
|![CompactTreeChart_out.vsdx](CompactTreeChart.png)|

### **Skapa ett organisationsschema med flödesdiagram**
 Layoutmetoden för[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page) klass autolayout formerna och kopplingarna på sidan som ett organisationsdiagram i flödesdiagramstil.

Koden nedan visar hur man:

1. Skapa ett diagram från stencil.
1. Lägg till organisationsnodformer på sidan.
1. Lägg till kopplingar till sidan för att koppla samman form och dess överordnade.
1. Automatisk layout genom att åberopa layoutmetoden
1. spara diagram
#### **Skapa ett flödesschema-stil Organisationsschema Programmeringsexempel**
Använd följande kod för att skapa ett organisationsschema med flödesdiagram med Aspose.Diagram.

```
{{< highlight "csharp" >}}
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
```

|**Resultat**|
|:- |
|![Flödesdiagram_ut.vsdx](FlowChart.png)|
