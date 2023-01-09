---
title: Ruby'de Visio Diagram'i XAML'e dışa aktar
type: docs
weight: 60
url: /tr/java/export-visio-diagram-to-xaml-in-ruby/
---
## **Aspose.Diagram - İhracat Visio Diagram ila XAML**
 Visio Diagram'i kullanarak XAML'e dışa aktarmak için**Yakut için Aspose.Diagram Java** , sadece çağırmak**ExportToXaml** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as XAML

diagram.save(data_dir + "Diagram.xaml", Rjb::import('com.aspose.diagram.SaveFileFormat').XAML)

puts "Exported visio diagram to XAML."

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Dışa aktarma Visio Diagram ila XAML (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoxaml.rb)
