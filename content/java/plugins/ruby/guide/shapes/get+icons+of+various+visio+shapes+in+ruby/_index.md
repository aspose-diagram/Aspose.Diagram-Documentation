---
title : "Get Icons of Various Visio Shapes in Ruby" 
description : "" 
weight : 20123 
toc : false
type: docs
url: /java/plugins/ruby/guide/shapes/get+icons+of+various+visio+shapes+in+ruby/
---

# Aspose.Diagram for Java : Get Icons of Various Visio Shapes in Ruby


## Aspose.Diagram - Get Icons of Various Visio Shapes

To Get Icons of Various Visio Shapes using **Aspose.Diagram Java for Ruby**, simply invoke **GetShapeIcon** module. Here you can see example code.

**Ruby Code**

data\_dir = File.dirname(File.dirname(File.dirname(File.dirname(\_\_FILE\_\_)))) + '/data/'# Create instance of Diagramdiagram = Rjb::import('com.aspose.diagram.Diagram').new(data\_dir + "Basic\_Shapes.vsd")# get mastermaster = diagram.getMasters().getMasterByName("Circle")# get byte arraybytes = master.getIcon()# create an image filefos = Rjb::import('java.io.FileOutputStream').new(data\_dir + "MyImage.png")# write byte array of the imagefos.write(bytes)# close arrayfos.close()puts "Get shape icon, please check the output file."

## Download Running Code

Download **Get Icons of Various Visio Shapes (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/getshapeicon.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Shapes/getshapeicon.rb)

