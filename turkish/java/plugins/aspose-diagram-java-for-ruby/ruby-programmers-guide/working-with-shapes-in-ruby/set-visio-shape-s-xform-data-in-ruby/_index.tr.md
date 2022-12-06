---
title: Visio Shape'in XForm Verilerini Ruby'de Ayarla
type: docs
weight: 150
url: /tr/java/set-visio-shape-s-xform-data-in-ruby/
---
## **Aspose.Diagram - Visio Shape'in XForm Verilerini Ayarla**
 Kullanarak Visio Shape'in XForm Verilerini Ayarlamak İçin**Yakut için Aspose.Diagram Java** , sadece çağırmak**SetShapeXFormData** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 veri_dir = Dosya.diradı(Dosya.diradı(Dosya.diradı(Dosya.diradı(__DOSYA__)))) + '/veri/'

\# Diagram örneğini oluştur

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

şekiller = diagram.getPages().getPage(0).getShapes()

ben = 0

 ben iken< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "process" && shape.getID() == 1

        shape.getXForm().getPinX().setValue(5)

        shape.getXForm().getPinY().setValue(5)

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "SetShapeXFormData.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set visio shape's XForm data."

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Shape'in XForm Verilerini Ayarla (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapexformdata.rb)
