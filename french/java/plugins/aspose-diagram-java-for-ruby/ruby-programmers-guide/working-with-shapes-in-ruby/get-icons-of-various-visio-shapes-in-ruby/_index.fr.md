---
title: Obtenez des icônes de diverses formes Visio en rubis
type: docs
weight: 40
url: /fr/java/get-icons-of-various-visio-shapes-in-ruby/
---
## **Aspose.Diagram - Obtenir des icônes de diverses formes Visio**
 Pour obtenir des icônes de diverses formes Visio à l'aide de**Aspose.Diagram Java pour rubis** , invoquez simplement**GetShapeIcon** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

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
## **Télécharger le code d'exécution**
 Télécharger**Obtenez des icônes de diverses formes Visio (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/getshapeicon.rb)
