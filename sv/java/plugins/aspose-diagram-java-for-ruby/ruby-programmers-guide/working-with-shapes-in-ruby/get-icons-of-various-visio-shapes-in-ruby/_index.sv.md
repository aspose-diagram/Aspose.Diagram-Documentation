---
title: Få ikoner av olika Visio former i rubin
type: docs
weight: 40
url: /sv/java/get-icons-of-various-visio-shapes-in-ruby/
---
## **Aspose.Diagram - Få ikoner av olika Visio former**
 För att få ikoner av olika Visio former med hjälp av**Aspose.Diagram Java för Ruby** , helt enkelt åberopa**GetShapeIcon** modul. Här kan du se exempelkod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Basic_Shapes.vsd")

\# get master

master = diagram.getMasters().getMasterByName("Circle")

\# get byte array

bytes = master.getIcon()

\# create an image file

fos = Rjb::import('java.io.FileOutputStream').new(data_dir + "MyImage.png")

\# write byte array of the image

fos.write(bytes)

\# close array

fos.close()

puts "Get shape icon, please check the output file."

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Få ikoner av olika Visio former (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/getshapeicon.rb)
