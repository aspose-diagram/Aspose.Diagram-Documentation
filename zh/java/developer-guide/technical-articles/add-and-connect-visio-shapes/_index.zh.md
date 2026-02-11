---
title: 添加和连接 Visio 形状
type: docs
weight: 10
url: /zh/java/add-and-connect-visio-shapes/
---
{{% alert color="primary" %}} 

Aspose.Diagram for Java 允许您添加自定义形状并将它们连接起来[你创建的图表](/diagram/zh/java/load-or-create-a-visio-drawing/).

{{% /alert %}} 
### **添加和连接形状**
下面示例中的代码显示了如何：

1. 创建一个 diagram。
1. 添加和自定义形状（矩形、星形、六边形）。
1. 将星形和六边形连接到矩形。
1. 保存 diagram。
#### **编程范例**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddConnectShapes.class);
        
// Load masters from any existing diagram, stencil or template
// and add in the new diagram
String visioStencil = dataDir + "AddConnectShapes.vss";
        
// Names of the masters present in the stencil
String rectangleMaster = "Rectangle", starMaster = "Star 7",
        hexagonMaster = "Hexagon", connectorMaster = "Dynamic connector";

int pageNumber = 0;
double width = 2, height = 2, pinX = 4.25, pinY = 9.5;

// Create a new diagram
Diagram diagram = new Diagram(visioStencil);

// Add a new rectangle shape
long rectangleId = diagram.addShape(
        pinX, pinY, width, height, rectangleMaster, pageNumber);

// Set the new shape's properties
Shape shape = diagram.getPages().getPage(pageNumber).getShapes().getShape(rectangleId);
shape.getText().getValue().add(new Txt("Rectangle text."));
shape.setName("Rectangle1");
shape.getXForm().getLocPinX().getUfe().setF("Width*0.5");
shape.getXForm().getLocPinY().getUfe().setF("Height*0.5");
shape.getLine().getLineColor().setValue("7");
shape.getLine().getLineWeight().setValue(0.03);
shape.getFill().getFillBkgnd().setValue("1");
shape.getFill().getFillForegnd().setValue("3");
shape.getFill().getFillPattern().setValue(31);

// Add a new star shape
pinX = 2.0;
pinY = 4.5;
long starId = diagram.addShape(
        pinX, pinY, width, height, starMaster, pageNumber);

// Set the star shape's properties
shape = diagram.getPages().getPage(pageNumber).getShapes().getShape(starId);
shape.getText().getValue().add(new Txt("Star text."));
shape.setName("Star1");
shape.getXForm().getLocPinX().getUfe().setF("Width*0.5");
shape.getXForm().getLocPinY().getUfe().setF("Height*0.5");
shape.getLine().getLineColor().setValue("#ff0000");
shape.getLine().getLineWeight().setValue(0.03);
shape.getFill().getFillBkgnd().setValue("#ff00ff");
shape.getFill().getFillForegnd().setValue("#0000ff");
shape.getFill().getFillPattern().setValue(31);

// Add a new hexagon shape
pinX = 7.0;
long hexagonId = diagram.addShape(
        pinX, pinY, width, height, hexagonMaster, pageNumber);

// Set the hexagon shape's properties
shape = diagram.getPages().getPage(pageNumber).getShapes().getShape(hexagonId);
shape.getText().getValue().add(new Txt("Hexagon text."));
shape.setName("Hexagon1");
shape.getXForm().getLocPinX().getUfe().setF("Width*0.5");
shape.getXForm().getLocPinY().getUfe().setF("Height*0.5");
shape.getLine().getLineWeight().setValue(0.03);
shape.getFill().getFillPattern().setValue(31);

// Add master to dynamic connector from the stencil
diagram.addMaster(visioStencil, connectorMaster);

// Connect rectangle and star shapes
Shape connector1 = new Shape();
long connecter1Id = diagram.addShape(connector1, connectorMaster, 0);
diagram.getPages().getPage(0).connectShapesViaConnector(rectangleId, ConnectionPointPlace.BOTTOM,
        starId, ConnectionPointPlace.TOP, connecter1Id);

// Connect rectangle and hexagon shapes
Shape connector2 = new Shape();
long connecter2Id = diagram.addShape(connector2, connectorMaster, 0);
diagram.getPages().getPage(0).connectShapesViaConnector(rectangleId, ConnectionPointPlace.BOTTOM,
        hexagonId, ConnectionPointPlace.LEFT, connecter2Id);

// Save the diagram
diagram.save(dataDir + "AddConnectShapes_Out.vsdx", SaveFileFormat.VDX);

{{< /highlight >}}

