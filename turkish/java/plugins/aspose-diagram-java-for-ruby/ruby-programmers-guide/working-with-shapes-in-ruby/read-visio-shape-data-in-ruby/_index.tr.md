---
title: Ruby'de Visio Şekil Verilerini Oku
type: docs
weight: 50
url: /tr/java/read-visio-shape-data-in-ruby/
---
## **Aspose.Diagram - Tüm Şekil Özelliklerini Oku**
 Kullanarak Tüm Şekil Özelliklerini Okumak İçin**Yakut için Aspose.Diagram Java** , aramak**read_all_shape_properties** yöntemi**ShapeData'yı Oku** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 kesin okuma_tüm_shape_properties()

 veri_dir = Dosya.diradı(Dosya.diradı(Dosya.diradı(Dosya.diradı(__DOSYA__)))) + '/veri/'

 # Diagram örneğini oluştur

 diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

 şekiller = diagram.getPages().getPage(0).getShapes()



 ben = 0

 ben iken< shapes.getCount()

        shape = shapes.get(i)

        if shape.getName() == "Process"

            j = 0

            while j < shape.getProps().getCount()

                property = shape.getProps().get(j)

                puts property.getLabel().getValue() + ": " + property.getValue().getVal()

                j +=1

            end

            break

        end

        i +=1

    end

end

{{< /highlight >}}
## **Aspose.Diagram - Ada Göre Şekil Özelliği Okuma**
 Bir Şekil Özelliğini Ada Göre Okumak için**Yakut için Aspose.Diagram Java** , aramak**read_shape_property_by_name** yöntemi**ShapeData'yı Oku** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 kesin okuma_şekil_Emlak_ile_isim()

 veri_dir = Dosya.diradı(Dosya.diradı(Dosya.diradı(Dosya.diradı(__DOSYA__)))) + '/veri/'

 # Diagram örneğini oluştur

 diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

 şekiller = diagram.getPages().getPage(0).getShapes()



 ben = 0

 ben iken< shapes.getCount()

        shape = shapes.get(i)

        if shape.getName() == "Process"

            property = shape.getProps().getProp("Cost")

            puts property.getLabel().getValue() + ": " + property.getValue().getVal()

        end

        i +=1

    end

end

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Şekil Verilerini Oku (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/readshapedata.rb)
