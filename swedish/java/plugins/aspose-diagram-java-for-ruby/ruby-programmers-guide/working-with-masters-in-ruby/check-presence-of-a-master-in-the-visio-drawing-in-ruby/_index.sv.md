---
title: Kontrollera närvaron av en mästare i Visio-ritningen i Ruby
type: docs
weight: 10
url: /sv/java/check-presence-of-a-master-in-the-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Kontrollera en masternärvaro med ID**
 För att kontrollera en masternärvaro med ID med hjälp av**Aspose.Diagram Java för Ruby** , ringa upp**check_presence_master_by_id** metod av**CheckPresenceOfMaster** modul. Här kan du se exempelkod.

**Ruby kod**

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
## **Aspose.Diagram - Kontrollera en masternärvaro efter namn**
 För att kontrollera en masternärvaro efter namn med hjälp av**Aspose.Diagram Java för Ruby** , ringa upp**check_presence_master_by_name** metod av**CheckPresenceOfMaster** modul. Här kan du se exempelkod.

**Ruby kod**

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
## **Ladda ner Running Code**
 Ladda ner**Kontrollera närvaron av en master i Visio-ritningen (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/checkpresenceofmaster.rb)
