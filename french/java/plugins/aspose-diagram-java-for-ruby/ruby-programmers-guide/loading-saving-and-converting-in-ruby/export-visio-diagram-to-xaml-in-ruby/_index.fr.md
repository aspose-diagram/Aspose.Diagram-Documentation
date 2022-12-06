---
title: Export Visio Diagram to XAML in Ruby
type: docs
weight: 60
url: /fr/java/export-visio-diagram-to-xaml-in-ruby/
---
## **Aspose.Diagram - Export Visio Diagram to XAML**
To Export Visio Diagram to XAML using **Aspose.Diagram Java pour rubis** , invoquez simplement**ExportToXaml** module. Ici vous pouvez voir un exemple de code.

**Code rubis**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as XAML

diagram.save(data_dir + "Diagram.xaml", Rjb::import('com.aspose.diagram.SaveFileFormat').XAML)

puts "Exported visio diagram to XAML."

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Export Visio Diagram to XAML (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoxaml.rb)
