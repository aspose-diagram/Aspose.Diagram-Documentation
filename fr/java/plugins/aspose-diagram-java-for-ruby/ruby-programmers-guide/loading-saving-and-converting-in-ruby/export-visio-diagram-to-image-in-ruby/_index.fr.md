---
title: Exporter Visio Diagram vers une image en Ruby
type: docs
weight: 30
url: /fr/java/export-visio-diagram-to-image-in-ruby/
---
## **Aspose.Diagram - Exporter Visio Diagram vers l'image**
 Pour exporter Visio Diagram vers une image à l'aide**Aspose.Diagram Java pour rubis** , invoquez simplement**Exporter vers l'image** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as PNG

diagram.save(data_dir + "Diagram.png", Rjb::import('com.aspose.diagram.SaveFileFormat').PNG)

puts "Exported visio diagram to PNG."

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Exporter Visio Diagram vers l'image (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoimage.rb)
