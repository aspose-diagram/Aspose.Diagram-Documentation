---
title: Ruby'de Çizim Yazı Tipi Bilgilerini Al
type: docs
weight: 30
url: /tr/java/retrieve-drawing-font-information-in-ruby/
---
## **Aspose.Diagram - Çizim Yazı Tipi Bilgilerini Al**
 Kullanarak Çizim Yazı Tipi Bilgilerini Almak İçin**Yakut için Aspose.Diagram Java** , sadece çağırmak**GetDiagramFontInfo** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 veri_dir = Dosya.diradı(Dosya.diradı(Dosya.diradı(Dosya.diradı(__DOSYA__)))) + '/veri/'

\# Diagram örneğini oluştur

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

yazı tipleri = diagram.getFonts()

ben = 0

 ben iken< fonts.getCount()

    font = fonts.get(i)

    # Display information about the fonts

    puts font.getName()

    i +=1

end

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Çizim Yazı Tipi Bilgilerini Al (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/getdiagramfontinfo.rb)
