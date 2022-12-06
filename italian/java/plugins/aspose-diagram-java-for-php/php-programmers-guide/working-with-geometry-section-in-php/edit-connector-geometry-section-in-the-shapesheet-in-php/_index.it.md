---
title: Modifica la sezione della geometria del connettore nello ShapeSheet in PHP
type: docs
weight: 10
url: /it/java/edit-connector-geometry-section-in-the-shapesheet-in-php/
---
## **Aspose.Diagram - Modifica sezione geometria connettore nello ShapeSheet**
 Per modificare la sezione della geometria del connettore nello ShapeSheet utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**ShapeGeometrySection** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

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
## **Scarica il codice in esecuzione**
 Scarica**Modifica sezione geometria connettore nello ShapeSheet (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithGeometrySection/ShapeGeometrySection.php)
