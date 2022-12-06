---
title: Ruby'de Visio Çiziminden Şekil Köprü Verilerini Alın
type: docs
weight: 20
url: /tr/java/get-shape-hyperlink-data-from-a-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Şekil Köprü Verilerini Al**
Kullanarak Şekil Köprü Verilerini Almak İçin**Yakut için Aspose.Diagram Java** , sadece çağırmak**GetShapeKöprüVerileri** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 veri_dir = Dosya.diradı(Dosya.diradı(Dosya.diradı(Dosya.diradı(__DOSYA__)))) + '/veri/'

\# Diagram örneğini oluştur

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Köprüler.vdx")

\# Belirli bir şekil al

şekil = diagram.getPages().getPage("Akış 1").getShapes().getShape(1)

köprüler = shape.getHyperlinks()

ben = 0

 ben iken< hyperlinks.getCount()

    hyperlink = hyperlinks.get(i)

    puts "Address: " + hyperlink.getAddress().getValue().to_s

    puts "Sub Address: " + hyperlink.getSubAddress().getValue().to_s

    puts "Description: " + hyperlink.getDescription().getValue().to_s

    i +=1

end

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Çiziminden (Aspose.Diagram) Shape Hyperlink Verilerini Alın**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Hyperlinks/getshapehyperlinkdata.rb)
