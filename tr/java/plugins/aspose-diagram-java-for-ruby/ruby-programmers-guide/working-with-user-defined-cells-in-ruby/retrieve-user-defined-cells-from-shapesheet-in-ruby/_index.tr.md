---
title: Ruby'de Şekil Sayfasından Kullanıcı Tanımlı Hücreleri Alın
type: docs
weight: 30
url: /tr/java/retrieve-user-defined-cells-from-shapesheet-in-ruby/
---
## **Aspose.Diagram - Şekil Sayfasından Kullanıcı Tanımlı Hücreleri Al**
 Kullanarak Şekil Sayfasından Kullanıcı Tanımlı Hücreleri Almak İçin**Yakut için Aspose.Diagram Java** , sadece çağırmak**GetUserDefinedCells** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 veri_dir = Dosya.diradı(Dosya.diradı(Dosya.diradı(Dosya.diradı(__DOSYA__)))) + '/veri/'

\# Diagram örneğini oluştur

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "UserDefinedCells.vdx")

sayfalar = diagram.getPages()

sayı = 0

 sayarken< pages.getCount()

    page = pages.get(count)

    shapes = page.getShapes()

    i = 0

    while i < shapes.getCount()

        shape = shapes.get(i)

        if shape.getNameU() == "Process"

            users = shape.getUsers()

            j = 0

            while j < users.getCount()

                user = users.get(j)

                            puts "Name: " + user.getNameU() + " Value: " + user.getValue().getVal() + " Prompt: " + user.getPrompt().getValue()

                j +=1

            end

            break

        end

        i +=1

    end

    count +=1

end

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Şekil Sayfasından Kullanıcı Tanımlı Hücreleri Al (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/getuserdefinedcells.rb)
