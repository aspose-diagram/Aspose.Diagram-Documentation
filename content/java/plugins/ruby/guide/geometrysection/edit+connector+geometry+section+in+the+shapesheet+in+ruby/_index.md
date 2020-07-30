---
title : "Edit Connector Geometry Section in the ShapeSheet in Ruby" 
description : "" 
weight : 20164 
toc : false
type: docs
url: /java/plugins/ruby/guide/geometrysection/edit+connector+geometry+section+in+the+shapesheet+in+ruby/
---

# Aspose.Diagram for Java : Edit Connector Geometry Section in the ShapeSheet in Ruby


## Aspose.Diagram - Edit Connector Geometry Section in the ShapeSheet

To Edit Connector Geometry Section in the ShapeSheet using **Aspose.Diagram Java for Ruby**, simply invoke **ShapeGeometrySection** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Call the diagram constructor to load diagram from a VSD filediagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Drawing.vsd")#set connector shape idconnector\_id = 1connector = diagram.getPages().getPage(0).getShapes().getShape(connector\_id)# get connector geometry at index 0defaultLineTo = connector.getGeoms().get(0).getCoordinateCol().getLineToCol().get(0)# remove connector geometry from index 0connector.getGeoms().get(0).getCoordinateCol().getLineToCol().get(0).setDel(1)# initialize LineTo geometry objectline\_to = Rjb::import('com.aspose.diagram.LineTo').new# set X valueline\_to.getX().setValue(0)# set Y valueline\_to.getY().setValue(defaultLineTo.getY().getValue() / 2)# add connector geometryconnector.getGeoms().get(0).getCoordinateCol().add(line\_to)# initialize LineTo geometry objectline\_to = Rjb::import('com.aspose.diagram.LineTo').new# set Y valueline\_to.getY().setValue(defaultLineTo.getY().getValue() / 2)# set X valueline\_to.getX().setValue(defaultLineTo.getX().getValue())# add connector geometryconnector.getGeoms().get(0).getCoordinateCol().add(line\_to)# initialize LineTo geometry objectline\_to = Rjb::import('com.aspose.diagram.LineTo').new# set X valueline\_to.getX().setValue(defaultLineTo.getX().getValue())# set Y valueline\_to.getY().setValue(defaultLineTo.getY().getValue())# add connector geometryconnector.getGeoms().get(0).getCoordinateCol().add(line\_to)# Save as Htmldiagram.save(data\_dir + "Geometry.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)puts "Updated Connector Geometry Section in the ShapeSheet."

## Download Running Code

Download **Edit Connector Geometry Section in the ShapeSheet (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Geometry/shapegeometrysection.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Geometry/shapegeometrysection.rb)

