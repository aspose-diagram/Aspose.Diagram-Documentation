---
title: Få Master Object från Drawing in Ruby
type: docs
weight: 20
url: /sv/java/get-master-object-from-drawing-in-ruby/
---
## **Aspose.Diagram - Få ett huvudobjekt med ID**
 För att få ett huvudobjekt med ID med hjälp av**Aspose.Diagram Java för Ruby** , ringa upp**get_master_object_by_id** metod av**GetMasterObject** modul. Här kan du se exempelkod.

**Ruby kod**

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
## **Aspose.Diagram - Få ett huvudobjekt efter namn**
 För att få ett huvudobjekt med namn med hjälp av**Aspose.Diagram Java för Ruby** , ringa upp**get_master_object_by_name** metod av**GetMasterObject** modul. Här kan du se exempelkod.

**Ruby kod**

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
## **Ladda ner Running Code**
 Ladda ner**Få huvudobjekt från ritning (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/getmasterobject.rb)
