---
title: Ruby'de Visio Şekil Metni Güncellemesi
type: docs
weight: 30
url: /tr/java/update-visio-shape-text-in-ruby/
---
## **Aspose.Diagram - Güncelleme Visio Şekil Metni**
Visio Shape Text'i kullanarak güncellemek için**Yakut için Aspose.Diagram Java** , sadece çağırmak**ShapeText'i Güncelle** modül. Burada örnek kodu görebilirsiniz.

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

        shape.getText().getValue().clear()

        shape.getText().getValue().add(Rjb::import('com.aspose.diagram.Txt').new("New Text"))

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "UpdateShapeText.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Updated shape text."

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Güncelleme Visio Şekil Metni (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Text/updateshapetext.rb)
