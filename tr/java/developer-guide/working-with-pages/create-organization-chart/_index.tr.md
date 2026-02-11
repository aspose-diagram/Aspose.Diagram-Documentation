---
title: Organizasyon Şeması Oluştur
type: docs
weight: 100
url: /tr/java/create-organization-chart/
description: Bu bölümde, Aspose.Diagram for Java kullanılarak bir organizasyon şemasının nasıl oluşturulacağı açıklanmaktadır.
---
## ** Bir Organizasyon Şeması Oluşturun**
Bu bölümde, Aspose.Diagram for Java kullanılarak bir organizasyon şemasının nasıl oluşturulacağı açıklanmaktadır.
### **CompactTree tarzı bir Organizasyon Şeması oluşturun**
 Düzen yöntemi[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)class, sayfadaki şekilleri ve bağlayıcıları bir CompactTree stili Organizasyon Şeması olarak otomatik olarak düzenler.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Şablondan bir diagram oluşturun.
1. Sayfaya kuruluş düğümü şekilleri ekleyin.
1. Şekli ve üst öğesini bağlamak için sayfaya bağlayıcılar ekleyin.
1. Düzen yöntemini çağırarak otomatik düzen
1. kaydet diagram
#### **CompactTree stili Organizasyon Şeması Programlama Örneği Oluşturma**
Aspose.Diagram for Java kullanarak bir CompactTree tarzı Organizasyon Şeması oluşturmak için aşağıdaki kodu kullanın.


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


|**Sonuç**|
|:- |
|![CompactTreeChart_out.vsdx](CompactTreeChart.png)|

### **Akış Şeması stilinde bir Organizasyon Şeması oluşturun**
 Düzen yöntemi[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) class, sayfadaki şekilleri ve bağlayıcıları bir Akış Şeması stili Organizasyon Şeması olarak otomatik olarak düzenler.

Aşağıdaki kod nasıl yapılacağını gösterir:

1. Şablondan bir diagram oluşturun.
1. Sayfaya kuruluş düğümü şekilleri ekleyin.
1. Şekli ve üst öğesini bağlamak için sayfaya bağlayıcılar ekleyin.
1. Düzen yöntemini çağırarak otomatik düzen
1. kaydet diagram
#### **Akış Şeması stili Organizasyon Şeması Programlama Örneği oluşturun**
Aspose.Diagram for Java kullanarak bir Akış Şeması stili Organizasyon Şeması oluşturmak için aşağıdaki kodu kullanın.


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


|**Sonuç**|
|:- |
|![Akış Şeması_out.vsdx](FlowChart.png)|
