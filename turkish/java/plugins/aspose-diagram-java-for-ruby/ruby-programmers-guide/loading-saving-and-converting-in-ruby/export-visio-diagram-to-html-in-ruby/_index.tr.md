---
title: Ruby'de Visio Diagram'i HTML'e dışa aktar
type: docs
weight: 20
url: /tr/java/export-visio-diagram-to-html-in-ruby/
---
## **Aspose.Diagram - İhracat Visio Diagram ila HTML**
 Visio Diagram'i kullanarak HTML'e dışa aktarmak için**Yakut için Aspose.Diagram Java** , sadece çağırmak**ExportToHtml** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as Html

diagram.save(data_dir + "Diagram.html", Rjb::import('com.aspose.diagram.SaveFileFormat').HTML)

puts "Exported visio diagram to HTML."

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Dışa aktarma Visio Diagram ila HTML (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttohtml.rb)
