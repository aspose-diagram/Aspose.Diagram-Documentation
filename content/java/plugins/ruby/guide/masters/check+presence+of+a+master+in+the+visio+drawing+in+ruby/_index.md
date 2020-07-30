---
title : "Check Presence of a Master in the Visio Drawing in Ruby" 
description : "" 
weight : 20106 
toc : false
type: docs
url: /java/plugins/ruby/guide/masters/check+presence+of+a+master+in+the+visio+drawing+in+ruby/
---

# Aspose.Diagram for Java : Check Presence of a Master in the Visio Drawing in Ruby


## Aspose.Diagram - Checking a Master Presence by ID

To Check a Master Presence by ID using **Aspose.Diagram Java for Ruby**, call **check\_presence\_master\_by\_id** method of **CheckPresenceOfMaster** module. Here you can see example code.

**Ruby Code**

{{< code lang="cs" >}}
def check_presence_master_by_id()
    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file
    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    master_id = 2
    # check master by id
    is_present = diagram.getMasters().isExist(master_id)

    puts "Master Presence : " + is_present.to_s
end
{{< /code >}}

## Aspose.Diagram - Checking a Master Presence by Name

To Check a Master Presence by Name using **Aspose.Diagram Java for Ruby**, call **check\_presence\_master\_by\_name** method of **CheckPresenceOfMaster** module. Here you can see example code.

**Ruby Code**

{{< code lang="cs" >}}
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
{{< /code >}}

## Download Running Code

Download **Check Presence of a Master in the Visio Drawing (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/checkpresenceofmaster.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Masters/checkpresenceofmaster.rb)

