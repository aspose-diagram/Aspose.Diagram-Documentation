---
title: Ruby'de Visio Çiziminde Master Varlığını Kontrol Edin
type: docs
weight: 10
url: /tr/java/check-presence-of-a-master-in-the-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Kimliğe Göre Bir Ana Varlığın Kontrol Edilmesi**
 Kimliğe göre bir Ana Varlığı Kontrol Etmek İçin**Yakut için Aspose.Diagram Java** , aramak**check_presence_master_by_id** yöntemi**CheckPresenceOfMaster** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 def check_presence_master_by_id()

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    master_id = 2

    # check master by id

    is_present = diagram.getMasters().isExist(master_id)

    puts "Master Presence : " + is_present.to_s

end

{{< /highlight >}}
## **Aspose.Diagram - Ada Göre Bir Ana Varlığın Kontrol Edilmesi**
 Bir Ana Varlığı Ada Göre Kontrol Etmek İçin**Yakut için Aspose.Diagram Java** , aramak**check_presence_master_by_name** yöntemi**CheckPresenceOfMaster** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 def check_presence_master_by_name()

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    # Set master name

    master_name = "Background tranquil .2"

    # check master object by name

    is_present = diagram.getMasters().isExist(master_name)

    puts "Master Presence : " + is_present.to_s

end

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Çiziminde Master Varlığını Kontrol Edin (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/checkpresenceofmaster.rb)
