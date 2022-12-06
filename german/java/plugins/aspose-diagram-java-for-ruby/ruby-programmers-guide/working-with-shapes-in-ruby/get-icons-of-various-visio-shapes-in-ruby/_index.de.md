---
title: Holen Sie sich Symbole verschiedener Visio-Formen in Ruby
type: docs
weight: 40
url: /de/java/get-icons-of-various-visio-shapes-in-ruby/
---
## **Aspose.Diagram - Holen Sie sich Symbole verschiedener Visio-Formen**
 Verwenden von Symbolen verschiedener Visio-Formen**Aspose.Diagram Java für Rubin** , einfach aufrufen**GetShapeIcon** Modul. Hier sehen Sie Beispielcode.

**Ruby-Code**

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
## **Laufcode herunterladen**
 Download**Holen Sie sich Symbole verschiedener Visio-Formen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/getshapeicon.rb)
