---
title: Ruby'de Bir Şeklin Konumunu Değiştirme
type: docs
weight: 10
url: /tr/java/change-the-position-of-a-shape-in-ruby/
---
## **Aspose.Diagram - Bir Şeklin Konumunu Değiştirme**
 Kullanarak Bir Şeklin Konumunu Değiştirmek İçin**Yakut için Aspose.Diagram Java** , sadece çağırmak**Şekil Konumunu Değiştir** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 veri_dir = Dosya.diradı(Dosya.diradı(Dosya.diradı(Dosya.diradı(__DOSYA__)))) + '/veri/'

\# Diagram örneğini oluştur

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

şekiller = diagram.getPages().getPage(0).getShapes()

ben = 0

 ben iken< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process" && shape.getID() == 2

        shape.move(1, 1)

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "ChangeShapePosition.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Changed position of a shape."

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Bir Şeklin Konumunu Değiştirme (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/changeshapeposition.rb)
