---
title: Ruby'de Bağlayıcı Şeklinin Yeniden Yönlendirme Seçeneğini Seçin
type: docs
weight: 90
url: /tr/java/select-reroute-option-of-the-connector-shape-in-ruby/
---
## **Aspose.Diagram - Bağlayıcı Şeklinin Yeniden Yönlendirme Seçeneğini Belirleyin**
 Kullanarak Bağlayıcı Şeklinin Yeniden Yönlendirme Seçeneğini Belirlemek İçin**Yakut için Aspose.Diagram Java** , sadece çağırmak**Yeniden Yönlendirme Seçeneği Seçin** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Access a particular page

page = diagram.getPages().getPage("Flow 1")

\# get a particular connector shape

shape = page.getShapes().getShape(1)

\# set reroute option

shape.getLayout().getConFixedCode().setValue(Rjb::import('com.aspose.diagram.ConFixedCodeValue').NEVER_REROUTE)

\# Save diagram

diagram.save(data_dir + "SelectRerouteOption.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Seleted reroute option of the connector shape."

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Konnektör Şeklinin Yeniden Yönlendirme Seçeneğini Belirleyin (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/selectrerouteoption.rb)
