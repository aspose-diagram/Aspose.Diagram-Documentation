---
title: Ruby'de Visio Diagram'i PDF'e dışa aktar
type: docs
weight: 40
url: /tr/java/export-visio-diagram-to-pdf-in-ruby/
---
## **Aspose.Diagram - İhracat Visio Diagram ila PDF**
 Visio Diagram'i kullanarak PDF'e dışa aktarmak için**Yakut için Aspose.Diagram Java** , sadece çağırmak**ExportToPdf** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as PDF file format

diagram.save(data_dir + "Diagram.pdf", Rjb::import('com.aspose.diagram.SaveFileFormat').PDF)

puts "Exported visio diagram to pdf."

{{< /highlight >}}
## **Çalışan Kodu İndir**
İndirmek**Dışa aktarma Visio Diagram ila PDF (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttopdf.rb)
