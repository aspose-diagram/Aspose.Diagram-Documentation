---
title: Organizasyon Şeması Oluştur
type: docs
weight: 100
url: /tr/net/create-organization-chart/
description: Bu bölümde, Aspose.Diagram kullanılarak bir organizasyon şemasının nasıl oluşturulacağı açıklanmaktadır.
---
## ** Bir Organizasyon Şeması Oluşturun**
Bu bölümde, Aspose.Diagram kullanılarak bir organizasyon şemasının nasıl oluşturulacağı açıklanmaktadır.
### **CompactTree tarzı bir Organizasyon Şeması oluşturun**
 Düzen yöntemi[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class, sayfadaki şekilleri ve bağlayıcıları bir CompactTree stili Organizasyon Şeması olarak otomatik olarak düzenler.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Şablondan bir diagram oluşturun.
1. Sayfaya kuruluş düğümü şekilleri ekleyin.
1. Şekli ve üst öğesini bağlamak için sayfaya bağlayıcılar ekleyin.
1. Düzen yöntemini çağırarak otomatik düzen
1. kaydet diagram
#### **CompactTree stili Organizasyon Şeması Programlama Örneği Oluşturma**
Aspose.Diagram kullanarak bir CompactTree tarzı Organizasyon Şeması oluşturmak için aşağıdaki kodu kullanın.

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

|**Sonuç**|
|:- |
|![CompactTreeChart_out.vsdx](CompactTreeChart.png)|

### **Akış Şeması stilinde bir Organizasyon Şeması oluşturun**
 Düzen yöntemi[Sayfa](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class, sayfadaki şekilleri ve bağlayıcıları bir Akış Şeması stili Organizasyon Şeması olarak otomatik olarak düzenler.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Şablondan bir diagram oluşturun.
1. Sayfaya kuruluş düğümü şekilleri ekleyin.
1. Şekli ve üst öğesini bağlamak için sayfaya bağlayıcılar ekleyin.
1. Düzen yöntemini çağırarak otomatik düzen
1. kaydet diagram
#### **Akış Şeması stili Organizasyon Şeması Programlama Örneği oluşturun**
Aspose.Diagram kullanarak bir Akış Şeması stili Organizasyon Şeması oluşturmak için aşağıdaki kodu kullanın.

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

|**Sonuç**|
|:- |
|![Akış Şeması_out.vsdx](FlowChart.png)|
