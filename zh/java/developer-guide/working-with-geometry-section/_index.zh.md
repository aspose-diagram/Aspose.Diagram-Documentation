---
title: 使用几何部分
type: docs
weight: 180
url: /zh/java/working-with-geometry-section/
---
## **修改连接器形状的几何部分**
Microsoft Office Visio 中的任何形状都是由一个或多个“几何图形”组成的。每个几何图形代表形状的不同组成部分。大多数形状只有一种几何形状，但有些形状有两种或更多。 Aspose.Diagram API 允许开发人员以编程方式管理这些几何图形。

下面的代码片段管理形状的几何形状。
### **编程范例**
下面的代码片段管理形状的几何形状。

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(EditConnectorGeometry.class);    
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//set connector shape id
long connectorId = 4;
Shape connector = diagram.getPages().getPage("Page-1").getShapes().getShape(connectorId);
//get connector geometry at index 0
LineTo defaultLineTo = connector.getGeoms().get(0).getCoordinateCol().getLineToCol().get(0);
//remove connector geometry from index 0
connector.getGeoms().get(0).getCoordinateCol().getLineToCol().get(0).setDel(BOOL.TRUE);

//initialize LineTo geometry object
LineTo lineTo = new LineTo();
//set X value
lineTo.getX().setValue(0);
//set Y value
lineTo.getY().setValue(defaultLineTo.getY().getValue() / 2);
//add connector geometry
connector.getGeoms().get(0).getCoordinateCol().add(lineTo);

//initialize LineTo geometry object
lineTo = new LineTo();
//set Y value
lineTo.getY().setValue(defaultLineTo.getY().getValue() / 2);
//set X value
lineTo.getX().setValue(defaultLineTo.getX().getValue());
//add connector geometry
connector.getGeoms().get(0).getCoordinateCol().add(lineTo);

//initialize LineTo geometry object
lineTo = new LineTo();
//set X value
lineTo.getX().setValue(defaultLineTo.getX().getValue());
//set Y value
lineTo.getY().setValue(defaultLineTo.getY().getValue());
//add connector geometry
connector.getGeoms().get(0).getCoordinateCol().add(lineTo);

//save diagram in VDX format
diagram.save(dataDir + "EditConnectorGeometry_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
