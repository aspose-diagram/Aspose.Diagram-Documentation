---
title: Visio Diagram'i Ruby'de XAML'ye aktar
type: docs
weight: 60
url: /tr/java/export-visio-diagram-to-xaml-in-ruby/
---
## **Aspose.Diagram - Visio Diagram'i XAML'ye aktar**
 Kullanarak Visio Diagram'i XAML'ye Dışa Aktarmak için**Yakut için Aspose.Diagram Java** , sadece çağırmak**ExportToXaml** modül. Burada örnek kodu görebilirsiniz.

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
 İndirmek**Visio Diagram'i XAML'ye (Aspose.Diagram) aktar**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoxaml.rb)
