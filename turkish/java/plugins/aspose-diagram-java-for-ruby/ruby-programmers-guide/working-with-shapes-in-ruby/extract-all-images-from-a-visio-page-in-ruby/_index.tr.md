---
title: Ruby'deki Visio Sayfasındaki Tüm Resimleri Çıkarın
type: docs
weight: 30
url: /tr/java/extract-all-images-from-a-visio-page-in-ruby/
---
## **Aspose.Diagram - Bir Visio Sayfasından Tüm Resimleri Çıkarın**
 Kullanarak Visio Sayfasından Tüm Görüntüleri Çıkarmak için**Yakut için Aspose.Diagram Java** , sadece çağırmak**Görüntüleri Ayıkla** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 veri_dir = Dosya.diradı(Dosya.diradı(Dosya.diradı(Dosya.diradı(__DOSYA__)))) + '/veri/'

\# Diagram örneğini oluştur

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

şekiller = diagram.getPages().getPage("Akış 1").getShapes()

ben = 0

 ben iken< shapes.getCount()

    shape = shapes.get(i)

    # Filter shapes by type Foreign

    if shape.getType() == Rjb::import('com.aspose.diagram.TypeValue').FOREIGN

        # create an image file

        fos = Rjb::import('java.io.FileOutputStream').new(data_dir + "Image#{i}.bmp")

        fos.write(shape.getForeignData().getValue())

        fos.close()

    end

    i +=1

end

puts "Extracted images successfully!"

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Bir Visio Sayfasından Tüm Resimleri Çıkarın (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/extractimages.rb)
