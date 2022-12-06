---
title: Ruby'de Bir Şeklin Yüksekliğini ve Genişliğini Ayarlama
type: docs
weight: 120
url: /tr/java/set-the-height-and-width-of-a-shape-in-ruby/
---
## **Aspose.Diagram - Bir Şeklin Yüksekliğini ve Genişliğini Ayarla**
 Bir Şeklin Yüksekliğini ve Genişliğini Ayarlamak için**Yakut için Aspose.Diagram Java** , sadece çağırmak**SetShapeHeightAndWidth** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 veri_dir = Dosya.diradı(Dosya.diradı(Dosya.diradı(Dosya.diradı(__DOSYA__)))) + '/veri/'

\# Diagram örneğini oluştur

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

şekiller = diagram.getPages().getPage(0).getShapes()

ben = 0

 ben iken< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process" && shape.getID() == 1

        shape.setWidth(2 * shape.getXForm().getWidth().getValue())

        shape.setHeight(2 * shape.getXForm().getHeight().getValue())

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "SetShapeHeightAndWidth.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set height and width of shape."

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Bir Şeklin Yüksekliğini ve Genişliğini Ayarlama (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapeheightandwidth.rb)
