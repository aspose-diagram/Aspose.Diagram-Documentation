---
title: Ruby'de Visio Çiziminden Sayfa Nesnesi Alın
type: docs
weight: 10
url: /tr/java/get-a-page-object-from-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Kimliğe Göre Sayfa Nesnesi Alma**
 Kullanarak kimliğe göre bir Sayfa Nesnesi Almak için**Yakut için Aspose.Diagram Java** , aramak**get_page_object_by_id** yöntemi**GetPageObject** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 def get_page_object_by_id() 

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    page_id = 0

    # Get page object by id

    page = diagram.getPages().getPage(page_id)

    puts "Page : " + page.to_string

end

{{< /highlight >}}
## **Aspose.Diagram - Ada Göre Sayfa Nesnesi Alma**
 Kullanarak Ada Göre Sayfa Nesnesi Almak İçin**Yakut için Aspose.Diagram Java** , aramak**get_page_object_by_name** yöntemi**GetPageObject** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 def get_page_object_by_name() 

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    # Set page name

    page_name = "Flow 1"

    # Get page object by name

    page = diagram.getPages().getPage(page_name)

    puts "Page : " + page.to_string

end

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Çiziminden (Aspose.Diagram) Sayfa Nesnesi Alın**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/getpageobject.rb)
