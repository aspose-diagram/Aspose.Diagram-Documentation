---
title: Export Visio Diagram to PDF in Ruby
type: docs
weight: 40
url: /fr/java/export-visio-diagram-to-pdf-in-ruby/
---
## **Aspose.Diagram - Export Visio Diagram to PDF**
To Export Visio Diagram to PDF using **Aspose.Diagram Java pour rubis** , invoquez simplement**ExporterVersPdf** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as PDF file format

diagram.save(data_dir + "Diagram.pdf", Rjb::import('com.aspose.diagram.SaveFileFormat').PDF)

puts "Exported visio diagram to pdf."

{{< /highlight >}}
## **Télécharger le code d'exécution**
Télécharger**Export Visio Diagram to PDF (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttopdf.rb)
