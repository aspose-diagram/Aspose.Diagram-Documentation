---
title: Ruby'de ShapeSheet'te Kullanıcı Tanımlı Hücre Oluşturma
type: docs
weight: 10
url: /tr/java/create-user-defined-cell-in-the-shapesheet-in-ruby/
---
## **Aspose.Diagram - ShapeSheet'te Kullanıcı Tanımlı Hücre Oluştur**
 Kullanarak ShapeSheet'te Kullanıcı Tanımlı Hücre Oluşturmak İçin**Yakut için Aspose.Diagram Java** , sadece çağırmak**Kullanıcı Tanımlı Hücre Oluştur** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 veri_dir = Dosya.diradı(Dosya.diradı(Dosya.diradı(Dosya.diradı(__DOSYA__)))) + '/veri/'

\# Diagram örneğini oluştur

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

sayfalar = diagram.getPages()

ben = 0

 ben iken< pages.getCount()

    page = pages.get(i)

    shapes = page.getShapes()

    j = 0

    while j < shapes.getCount()

        shape = shapes.get(j)

        if shape.getNameU() == "Process"

            # Initialize user object

            user = Rjb::import('com.aspose.diagram.User').new

            user.setName("UserDefineCell")

            user.getValue().setVal("800")

            # Add user-defined cell

            shape.getUsers().add(user)

        end

        j +=1

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "UserDefinedCells.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Created User-defined Cell in the ShapeSheet."

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**ShapeSheet'te Kullanıcı Tanımlı Hücre Oluşturun (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/createuserdefinedcell.rb)
