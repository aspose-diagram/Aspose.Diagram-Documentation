---
title: Visio Diagram'i Ruby'de Görüntüye Aktar
type: docs
weight: 30
url: /tr/java/export-visio-diagram-to-image-in-ruby/
---
## **Aspose.Diagram - Visio Diagram'i Resme Aktar**
 Visio Diagram'i kullanarak Görüntüye Dışa Aktarmak için**Yakut için Aspose.Diagram Java** , sadece çağırmak**Görüntüye Dışa Aktar** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as PNG

diagram.save(data_dir + "Diagram.png", Rjb::import('com.aspose.diagram.SaveFileFormat').PNG)

puts "Exported visio diagram to PNG."

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Diagram'i Resme Aktar (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoimage.rb)
