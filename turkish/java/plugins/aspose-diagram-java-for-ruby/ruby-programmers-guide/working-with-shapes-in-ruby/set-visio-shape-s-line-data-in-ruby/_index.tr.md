---
title: Visio Şeklin Çizgi Verilerini Ruby'de Ayarla
type: docs
weight: 140
url: /tr/java/set-visio-shape-s-line-data-in-ruby/
---
## **Aspose.Diagram - Visio Şeklin Satır Verilerini Ayarla**
 Visio Şeklin Çizgi Verisini Ayarlamak için**Yakut için Aspose.Diagram Java** , sadece çağırmak**SetShapeLineData** modül. Burada örnek kodu görebilirsiniz.

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

        shape.getLine().getLineColor().setValue(diagram.getPages().getPage(0).getShapes().getShape(1).getFill().getFillForegnd().getValue())

        shape.getLine().getLineWeight().setValue(0.07041666666666667)

        shape.getLine().getRounding().setValue(0.1)

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "SetShapeLineData.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set visio shape's line data."

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Şeklin Çizgi Verisini Ayarla (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapelinedata.rb)
