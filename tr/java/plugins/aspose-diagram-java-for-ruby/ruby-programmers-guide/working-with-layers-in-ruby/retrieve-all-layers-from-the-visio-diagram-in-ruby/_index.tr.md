---
title: Ruby'deki Visio Diagram'den Tüm Katmanları Alın
type: docs
weight: 30
url: /tr/java/retrieve-all-layers-from-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Tüm Katmanları Al**
 Kullanarak Tüm Katmanları Almak İçin**Yakut için Aspose.Diagram Java** , sadece çağırmak**Tüm Katmanları Getir** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 veri_dir = Dosya.diradı(Dosya.diradı(Dosya.diradı(Dosya.diradı(__DOSYA__)))) + '/veri/'

\# Diagram örneğini oluştur

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Visio sayfasını al

sayfa = diagram.getPages().getPage(0)

katmanlar = page.getPageSheet().getLayers()

ben = 0

 ben iken< layers.getCount()

    layer = layers.get(i)

    puts "Name: " + layer.getName().getValue().to_s

    puts "Visibility: " + layer.getVisible().getValue().to_s

    puts "Status: " + layer.getStatus().getValue().to_s



    i +=1

end

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Diagram'den (Aspose.Diagram) Tüm Katmanları Alın**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Layers/getalllayers.rb)
