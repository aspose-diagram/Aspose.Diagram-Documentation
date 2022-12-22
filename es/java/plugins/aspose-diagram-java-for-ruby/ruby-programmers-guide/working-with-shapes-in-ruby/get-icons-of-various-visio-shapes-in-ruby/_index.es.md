---
title: Obtenga íconos de varias formas Visio en Ruby
type: docs
weight: 40
url: /es/java/get-icons-of-various-visio-shapes-in-ruby/
---
## **Aspose.Diagram - Obtenga iconos de varias formas Visio**
 Para obtener íconos de varias formas Visio usando**Aspose.Diagram Java para rubí** , simplemente invocar**ObtenerIconoForma** módulo. Aquí puedes ver el código de ejemplo.

**código rubí**

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
## **Descargar código de ejecución**
 Descargar**Obtenga íconos de varias formas Visio (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/getshapeicon.rb)
