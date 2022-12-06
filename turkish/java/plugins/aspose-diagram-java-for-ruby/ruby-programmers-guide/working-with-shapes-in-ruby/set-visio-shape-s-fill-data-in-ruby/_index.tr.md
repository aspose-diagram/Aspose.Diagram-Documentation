---
title: Ruby'de Visio Shape's Fill verilerini ayarla
type: docs
weight: 130
url: /tr/java/set-visio-shape-s-fill-data-in-ruby/
---
## **Aspose.Diagram - Visio Shape's Fill verilerini ayarla**
 Visio Shape's Fill verilerini kullanarak ayarlamak için**Yakut için Aspose.Diagram Java** , sadece çağırmak**SetShapeFillData** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 veri_dir = Dosya.diradı(Dosya.diradı(Dosya.diradı(Dosya.diradı(__DOSYA__)))) + '/veri/'

\# Diagram örneğini oluştur

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

şekiller = diagram.getPages().getPage(0).getShapes()

ben = 0

 ben iken< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "rectangle" && shape.getID() == 1

        shape.getFill().getFillBkgnd().setValue(diagram.getPages().getPage(0).getShapes().getShape(0).getFill().getFillBkgnd().getValue())

        shape.getFill().getFillForegnd().setValue("#ebf8df")

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "SetShapeFillData.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set visio shape's fill data."

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Shape's Fill verilerini ayarla (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapefilldata.rb)
