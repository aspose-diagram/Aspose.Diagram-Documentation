---
title: Export Visio Diagram to HTML in Ruby
type: docs
weight: 20
url: /fr/java/export-visio-diagram-to-html-in-ruby/
---
## **Aspose.Diagram - Export Visio Diagram to HTML**
To Export Visio Diagram to HTML using **Aspose.Diagram Java pour rubis** , invoquez simplement**ExporterVersHtml** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as Html

diagram.save(data_dir + "Diagram.html", Rjb::import('com.aspose.diagram.SaveFileFormat').HTML)

puts "Exported visio diagram to HTML."

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Export Visio Diagram to HTML (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttohtml.rb)
