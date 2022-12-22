---
title: Ruby'de Visio'de Katmanlarla Şekil Nesnelerini Yapılandırma
type: docs
weight: 20
url: /tr/java/configure-shape-objects-with-layers-in-visio-in-ruby/
---
## **Aspose.Diagram - Şekil Nesnelerini Katmanlarla Yapılandırma**
 Kullanarak Katmanlarla Şekil Nesnelerini Yapılandırmak İçin**Yakut için Aspose.Diagram Java** , sadece çağırmak**ShapeWithLayers'ı Yapılandır** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 veri_dir = Dosya.diradı(Dosya.diradı(Dosya.diradı(Dosya.diradı(__DOSYA__)))) + '/veri/'

\# Diagram örneğini oluştur

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

şekiller = diagram.getPages().getPage("Akış 1").getShapes()

ben = 0

 ben iken< shapes.getCount()

    shape = shapes.get(i)

    #puts shape.getName().to_s

    if shape.getName() == "Process"

        # Add shape1 in first two layers. Here "0;1" are indexes of the layers

        layer = shape.getLayerMem()

        layer.getLayerMember().setValue("0;1")

    elsif shape.getName() == "Preparation"

        # Remove shape2 from all the layers

        layer = shape.getLayerMem()

        layer.getLayerMember().setValue("")

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "Layers.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Configured Shape Objects with Layers in Visio."

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio'de (Aspose.Diagram) Katmanlarla Şekil Nesnelerini Yapılandırma**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Layers/configureshapewithlayers.rb)
