---
title: Ruby'de Visio Diagram'i SVG'ye dışa aktar
type: docs
weight: 50
url: /tr/java/export-visio-diagram-to-svg-in-ruby/
---
## **Aspose.Diagram - Visio Diagram'i SVG'ye aktar**
 Visio Diagram'i kullanarak SVG'ye dışa aktarmak için**Yakut için Aspose.Diagram Java** , sadece çağırmak**ExportToSvg** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as SVG

diagram.save(data_dir + "Diagram.svg", Rjb::import('com.aspose.diagram.SaveFileFormat').SVG)

puts "Exported visio diagram to SVG."

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Diagram'i SVG'ye aktar (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttosvg.rb)
