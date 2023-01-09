---
title: Ruby'de Çizimden Ana Nesneyi Alın
type: docs
weight: 20
url: /tr/java/get-master-object-from-drawing-in-ruby/
---
## **Aspose.Diagram - Kimliğe Göre Ana Nesne Alma**
 Kullanarak kimliğe göre bir Ana Nesne Almak için**Yakut için Aspose.Diagram Java** , aramak**get_master_object_by_id** yöntemi**GetMasterObject** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 def get_master_object_by_id()

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    master_id = 2

    # Get master object by id

    master = diagram.getMasters().getMaster(master_id)

    puts "Master ID : " + master.getID().to_s

    puts "Master Name : " + master.getName().to_s

end

{{< /highlight >}}
## **Aspose.Diagram - Ada Göre Ana Nesne Alma**
 Kullanarak Ada Göre Bir Ana Nesne Almak İçin**Yakut için Aspose.Diagram Java** , aramak**get_master_object_by_name** yöntemi**GetMasterObject** modül. Burada örnek kodu görebilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 def get_master_object_by_name()

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    # Set master name

    master_name = "Background tranquil .2"

    # Get master object by name

    master = diagram.getMasters().getMasterByName(master_name)

    puts "Master ID : " + master.getID().to_s

    puts "Master Name : " + master.getName().to_s

end

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Çizimden Ana Nesneyi Al (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/getmasterobject.rb)
