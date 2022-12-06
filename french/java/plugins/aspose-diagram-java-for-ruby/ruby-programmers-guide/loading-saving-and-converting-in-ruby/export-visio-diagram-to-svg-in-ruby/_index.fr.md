---
title: Export Visio Diagram to SVG in Ruby
type: docs
weight: 50
url: /fr/java/export-visio-diagram-to-svg-in-ruby/
---
## **Aspose.Diagram - Export Visio Diagram to SVG**
To Export Visio Diagram to SVG using **Aspose.Diagram Java pour rubis** , invoquez simplement**Exporter vers Svg** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as SVG

diagram.save(data_dir + "Diagram.svg", Rjb::import('com.aspose.diagram.SaveFileFormat').SVG)

puts "Exported visio diagram to SVG."

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Export Visio Diagram to SVG (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttosvg.rb)
