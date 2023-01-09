---
title: Edite la sección de geometría del conector en ShapeSheet en Ruby
type: docs
weight: 10
url: /es/java/edit-connector-geometry-section-in-the-shapesheet-in-ruby/
---
## **Aspose.Diagram - Editar la sección de geometría del conector en ShapeSheet**
 Para editar la sección de geometría del conector en ShapeSheet usando**Aspose.Diagram Java para rubí** , simplemente invocar**FormaGeometríaSección** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

# set connector shape id

connector_id = 1

connector = diagram.getPages().getPage(0).getShapes().getShape(connector_id)

\# get connector geometry at index 0

defaultLineTo = connector.getGeoms().get(0).getCoordinateCol().getLineToCol().get(0)

\# remove connector geometry from index 0

connector.getGeoms().get(0).getCoordinateCol().getLineToCol().get(0).setDel(1)

\# initialize LineTo geometry object

line_to = Rjb::import('com.aspose.diagram.LineTo').new

\# set X value

line_to.getX().setValue(0)

\# set Y value

line_to.getY().setValue(defaultLineTo.getY().getValue() / 2)

\# add connector geometry

connector.getGeoms().get(0).getCoordinateCol().add(line_to)

\# initialize LineTo geometry object

line_to = Rjb::import('com.aspose.diagram.LineTo').new

\# set Y value

line_to.getY().setValue(defaultLineTo.getY().getValue() / 2)

\# set X value

line_to.getX().setValue(defaultLineTo.getX().getValue())

\# add connector geometry

connector.getGeoms().get(0).getCoordinateCol().add(line_to)

\# initialize LineTo geometry object

line_to = Rjb::import('com.aspose.diagram.LineTo').new

\# set X value

line_to.getX().setValue(defaultLineTo.getX().getValue())

\# set Y value

line_to.getY().setValue(defaultLineTo.getY().getValue())

\# add connector geometry

connector.getGeoms().get(0).getCoordinateCol().add(line_to)

\# Save as Html

diagram.save(data_dir + "Geometry.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Updated Connector Geometry Section in the ShapeSheet."

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Editar la sección de geometría del conector en ShapeSheet (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Geometry/shapegeometrysection.rb)
