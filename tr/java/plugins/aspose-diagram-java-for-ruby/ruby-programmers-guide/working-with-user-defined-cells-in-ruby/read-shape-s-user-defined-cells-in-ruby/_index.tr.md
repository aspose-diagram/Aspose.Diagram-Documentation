---
title: Ruby'de Şeklin Kullanıcı Tanımlı Hücrelerini Okuyun
type: docs
weight: 20
url: /tr/java/read-shape-s-user-defined-cells-in-ruby/
---
## **Aspose.Diagram - Şeklin Kullanıcı Tanımlı Hücrelerini Oku**
 Kullanarak Şeklin Kullanıcı Tanımlı Hücrelerini Okumak için**Yakut için Aspose.Diagram Java** , sadece çağırmak**ReadUserDefinedCells** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 veri_dir = Dosya.diradı(Dosya.diradı(Dosya.diradı(Dosya.diradı(__DOSYA__)))) + '/veri/'

\# Diagram örneğini oluştur

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "UserDefinedCells.vdx")

şekiller = diagram.getPages().getPage("Akış 1").getShapes()

ben = 0

 ben iken< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process"

        users = shape.getUsers()

        j = 0

        while j < users.getCount()

            user = users.get(j)

            puts user.getName() + ": " + user.getValue().getVal()

            j +=1

        end

        break

    end

    i +=1

end

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Şeklin Kullanıcı Tanımlı Hücrelerini Oku (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/readuserdefinedcells.rb)
