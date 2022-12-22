---
title: Ruby'de Master Bilgilerini Alın
type: docs
weight: 30
url: /tr/java/retrieve-the-masters-information-in-ruby/
---
## **Aspose.Diagram - Master Bilgilerini Al**
 Kullanarak Master Bilgilerini Almak için**Yakut için Aspose.Diagram Java** , sadece çağırmak**GetMasterInfo** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 veri_dir = Dosya.diradı(Dosya.diradı(Dosya.diradı(Dosya.diradı(__DOSYA__)))) + '/veri/'

\# Bir VSD dosyasından diagram yüklemek için diagram yapıcısını çağırın

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

ustalar = diagram.getMasters()

ben = 0

 ben iken< masters.getCount()

    master = masters.get(i)

    puts "Master ID : " + master.getID().to_s

    puts "Master Name : " + master.getName().to_s

    i +=1

end

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Master Bilgilerini Alın (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/getmasterinfo.rb)
