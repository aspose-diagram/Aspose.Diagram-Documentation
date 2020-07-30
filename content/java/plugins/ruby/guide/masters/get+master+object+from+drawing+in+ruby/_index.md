---
title : "Get Master Object from Drawing in Ruby" 
description : "" 
weight : 20107 
toc : false
type: docs
url: /java/plugins/ruby/guide/masters/get+master+object+from+drawing+in+ruby/
---

# Aspose.Diagram for Java : Get Master Object from Drawing in Ruby


## Aspose.Diagram - Getting a Master Object by ID

To Get a Master Object by ID using **Aspose.Diagram Java for Ruby**, call **get\_master\_object\_by\_id** method of **GetMasterObject** module. Here you can see example code.

**Ruby Code**

{{< code lang="cs" >}}
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
{{< /code >}}

## Aspose.Diagram - Getting a Master Object by Name

To Get a Master Object by Name using **Aspose.Diagram Java for Ruby**, call **get\_master\_object\_by\_name** method of **GetMasterObject** module. Here you can see example code.

**Ruby Code**

{{< code lang="cs" >}}
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
{{< /code >}}

## Download Running Code

Download **Get Master Object from Drawing (Aspose.Diagram)** from any of the below mentioned social coding sites:

*   [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/getmasterobject.rb)
*   [CodePlex](https://asposediagramjavaruby.codeplex.com/SourceControl/latest#lib/asposediagramjava/Masters/getmasterobject.rb)

