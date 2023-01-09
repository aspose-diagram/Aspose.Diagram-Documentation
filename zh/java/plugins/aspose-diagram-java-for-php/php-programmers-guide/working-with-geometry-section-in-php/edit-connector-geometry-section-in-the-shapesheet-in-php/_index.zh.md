---
title: 在 PHP 中编辑 ShapeSheet 中的连接器几何部分
type: docs
weight: 10
url: /zh/java/edit-connector-geometry-section-in-the-shapesheet-in-php/
---
## **Aspose.Diagram - 编辑 ShapeSheet 中的连接器几何部分**
要使用 ShapeSheet 中的编辑连接器几何部分**Aspose.Diagram Java 用于 PHP** 只需调用**形状几何部分**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram=new Diagram($dataDir."Drawing.vsd");

# set connector shape id

$connector_id=1;

$connector=$diagram->getPages()->getPage(0)->getShapes()->getShape($connector_id);

\# get connector geometry at index 0

$defaultLineTo=$connector->getGeoms()->get(0)->getCoordinateCol()->getLineToCol()->get(0);

\# remove connector geometry from index 0

$connector->getGeoms()->get(0)->getCoordinateCol()->getLineToCol()->get(0)->setDel(1);

\# initialize LineTo geometry object

$line_to = new LineTo();

\# set X value

$line_to->getX()->setValue(0);

\# set Y value

$line_to->getY()->setValue((int)(string)$defaultLineTo->getY()->getValue()/ 2);

\# add connector geometry

$connector->getGeoms()->get(0)->getCoordinateCol()->add($line_to);

\# initialize LineTo geometry object

$line_to=new LineTo();

\# set Y value

$line_to->getY()->setValue((int)(string)$defaultLineTo->getY()->getValue()/2);

\# set X value

$line_to->getX()->setValue($defaultLineTo->getX()->getValue());

\# add connector geometry

$connector->getGeoms()->get(0)->getCoordinateCol()->add($line_to);

\# initialize LineTo geometry object

$line_to = new LineTo();

\# set X value

$line_to->getX()->setValue($defaultLineTo->getX()->getValue());

\# set Y value

$line_to->getY()->setValue($defaultLineTo->getY()->getValue());

\# add connector geometry

$connector->getGeoms()->get(0)->getCoordinateCol()->add($line_to);

\# Save as Html

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Geometry.vdx",$saveFileFormat->VDX);

print "Updated Connector Geometry Section in the ShapeSheet.".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**在 ShapeSheet 中编辑连接器几何部分 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithGeometrySection/ShapeGeometrySection.php)
