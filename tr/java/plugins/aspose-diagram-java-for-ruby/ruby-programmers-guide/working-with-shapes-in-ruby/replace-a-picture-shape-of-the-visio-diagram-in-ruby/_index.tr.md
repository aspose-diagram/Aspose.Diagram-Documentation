---
title: Ruby'de Visio Diagram'in Resim Şeklini Değiştirme
type: docs
weight: 60
url: /tr/java/replace-a-picture-shape-of-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - Visio Diagram'in Resim Şeklini Değiştirme**
 Visio Diagram'in Resim Şeklini Değiştirmek İçin**Yakut için Aspose.Diagram Java** , sadece çağırmak**Resim Şeklini Değiştir** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 veri_dir = Dosya.diradı(Dosya.diradı(Dosya.diradı(Dosya.diradı(__DOSYA__)))) + '/veri/'

\# Diagram örneğini oluştur

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# görüntüyü bayt dizisine dönüştür

fi = Rjb::import('java.io.File').new(data_dir + "star.png")

file_content = Rjb::import('java.nio.file.Files').readAllBytes(fi.toPath())

şekiller = diagram.getPages().getPage("Akış 1").getShapes()

ben = 0

 ben iken< shapes.getCount()

    shape = shapes.get(i)

    # Filter shapes by type Foreign

    if shape.getType() == Rjb::import('com.aspose.diagram.TypeValue').FOREIGN

        # replace picture shape

        shape.getForeignData().setValue(file_content)

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "ReplacePictureShape.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Replaced picture shape successfully!"

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Diagram'in (Aspose.Diagram) Resim Şeklini Değiştirme**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/replacepictureshape.rb)
