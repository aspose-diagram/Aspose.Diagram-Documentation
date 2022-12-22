---
title: Ruby'de Visio Bağlayıcı Bilgilerini Alın
type: docs
weight: 20
url: /tr/java/retrieve-visio-connectors-information-in-ruby/
---
## **Aspose.Diagram - Visio Konnektör Bilgilerini Alın**
 Kullanarak Visio Konnektör Bilgilerini Almak İçin**Yakut için Aspose.Diagram Java** , sadece çağırmak**GetConnectorsInfo** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 veri_dir = Dosya.diradı(Dosya.diradı(Dosya.diradı(Dosya.diradı(__DOSYA__)))) + '/veri/'

\# Diagram örneğini oluştur

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

bağlayıcılar = diagram.getPages().getPage(0).getConnects()

ben = 0

 ben iken< connectors.getCount()

    connector = connectors.get(i)

    # Display information about the Connectors

    puts "From Shape ID : " + connector.getFromSheet().to_s

    puts "To Shape ID : " + connector.getToSheet().to_s

    i +=1

end

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Konnektör Bilgilerini Alın (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/getconnectorsinfo.rb)

