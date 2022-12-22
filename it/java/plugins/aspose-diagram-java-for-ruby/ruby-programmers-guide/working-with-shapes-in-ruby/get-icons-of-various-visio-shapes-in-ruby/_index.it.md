---
title: Ottieni icone di varie forme Visio in Ruby
type: docs
weight: 40
url: /it/java/get-icons-of-various-visio-shapes-in-ruby/
---
## **Aspose.Diagram - Ottieni icone di varie forme Visio**
 Per ottenere icone di varie forme Visio utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**GetShapeIcon** modulo. Qui puoi vedere il codice di esempio.

**Codice Rubino**

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
## **Scarica il codice in esecuzione**
 Scarica**Ottieni icone di varie forme Visio (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/getshapeicon.rb)
