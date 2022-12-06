---
title: Export Visio Diagram to XPS in Ruby
type: docs
weight: 80
url: /fr/java/export-visio-diagram-to-xps-in-ruby/
---
## **Aspose.Diagram - Export Visio Diagram to XPS**
To Export Visio Diagram to XPS using **Aspose.Diagram Java pour rubis** , invoquez simplement**Exporter vers Xps** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as XPS

diagram.save(data_dir + "Diagram.xps", Rjb::import('com.aspose.diagram.SaveFileFormat').XPS)

puts "Exported visio diagram to XPS."

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Export Visio Diagram to XPS (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoxps.rb)
