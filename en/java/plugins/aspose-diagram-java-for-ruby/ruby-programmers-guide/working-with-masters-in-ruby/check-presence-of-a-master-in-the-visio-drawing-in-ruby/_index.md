---
title: Check Presence of a Master in the Visio Drawing in Ruby
type: docs
weight: 10
url: /java/check-presence-of-a-master-in-the-visio-drawing-in-ruby/
---

## **Aspose.Diagram - Checking a Master Presence by ID**
To Check a Master Presence by ID using **Aspose.Diagram Java for Ruby**, call **check_presence_master_by_id** method of **CheckPresenceOfMaster** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

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
## **Aspose.Diagram - Checking a Master Presence by Name**
To Check a Master Presence by Name using **Aspose.Diagram Java for Ruby**, call **check_presence_master_by_name** method of **CheckPresenceOfMaster** module. Here you can see example code.

**Ruby Code**

{{< highlight ruby >}}

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
## **Download Running Code**
Download **Check Presence of a Master in the Visio Drawing (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/checkpresenceofmaster.rb)
