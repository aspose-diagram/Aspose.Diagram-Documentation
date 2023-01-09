---
title: Ruby'de Visio Çizimine Yeni Bir Boş Sayfa Ekleme
type: docs
weight: 20
url: /tr/java/insert-a-new-blank-page-into-a-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Visio Çizimine Yeni Bir Boş Sayfa Ekleyin**
 Kullanarak Visio Çizimine Yeni Bir Boş Sayfa Eklemek İçin**Yakut için Aspose.Diagram Java** , sadece çağırmak**Sayfa ekle** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 def başlat()

 veri_dir = Dosya.diradı(Dosya.diradı(Dosya.diradı(Dosya.diradı(__DOSYA__)))) + '/veri/'

 Bir VSD dosyasından diagram yüklemek için diagram yapıcısını çağırın

 diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

 # Maksimum sayfa kimliğini al

 maks._sayfa_kimlik = al_maks._sayfa_kimliği(diagram)

 # Yeni bir sayfa nesnesi başlat

 new_page = Rjb::import('com.aspose.diagram.Page').new

 # Adı ayarla

 new_page.setName("yeni sayfa")



 # Sayfa kimliğini ayarla

 yeni_sayfa.setID(maks._sayfa_kimliği + 1)

 # Veya Sayfa oluşturucuyu deneyin

 # Sayfa yeniSayfa = yeni Sayfa(MaxPageId + 1);

 # Yeni bir boş sayfa ekleyin

 diagram.getPages().add(yeni_sayfa)

 # Kaydet diagram

 diagram.kaydet(veri_dir + "Yeni Sayfa_Çıktı.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

 "Yeni sayfa eklendi."

son

kesinlikle al_maks._sayfa_kimliği(diagram)

maks = diagram.getPages().getPage(0).getID()

 ben = 1

 ben iken< diagram.getPages().getCount()

        if max < diagram.getPages().getPage(i).getID()

            max = diagram.getPages().getPage(i).getID()

        end

        i +=1

    end

    return max

end

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Çizimine Yeni Bir Boş Sayfa Ekleme (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/addpage.rb)
