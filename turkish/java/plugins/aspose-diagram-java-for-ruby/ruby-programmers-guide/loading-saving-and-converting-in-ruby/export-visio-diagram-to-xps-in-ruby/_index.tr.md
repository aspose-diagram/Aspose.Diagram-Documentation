---
title: Visio Diagram'i Ruby'de XPS'ye aktar
type: docs
weight: 80
url: /tr/java/export-visio-diagram-to-xps-in-ruby/
---
## **Aspose.Diagram - Visio Diagram'i XPS'ye aktar**
 Visio Diagram'i kullanarak XPS'e Aktarmak için**Yakut için Aspose.Diagram Java** , sadece çağırmak**ExportToXps** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as XPS

diagram.save(data_dir + "Diagram.xps", Rjb::import('com.aspose.diagram.SaveFileFormat').XPS)

puts "Exported visio diagram to XPS."

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Diagram'i XPS'ye (Aspose.Diagram) aktar**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoxps.rb)
