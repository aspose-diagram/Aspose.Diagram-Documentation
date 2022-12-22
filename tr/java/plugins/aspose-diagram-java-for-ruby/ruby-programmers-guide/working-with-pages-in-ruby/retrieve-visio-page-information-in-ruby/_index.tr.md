---
title: Ruby'de Visio Sayfa Bilgisini Alın
type: docs
weight: 30
url: /tr/java/retrieve-visio-page-information-in-ruby/
---
## **Aspose.Diagram - Visio Sayfa Bilgisini Al**
 Kullanarak Visio Sayfa Bilgilerini Almak İçin**Yakut için Aspose.Diagram Java** , sadece çağırmak**GetPageInfo** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

# page = diagram.getPages().getPage(page_id)

page = diagram.getPages().getPage(0)

puts "Page ID : " + page.getName().to_s

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Sayfa Bilgisini Al (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/getpageinfo.rb)
