---
title: 从 Ruby 绘图中获取主对象
type: docs
weight: 20
url: /zh/java/get-master-object-from-drawing-in-ruby/
---
## **Aspose.Diagram - 通过 ID 获取主对象**
要使用 ID 通过 ID 获取主对象**Aspose.Diagram Java 红宝石**， 称呼**get_master_object_by_id 获取**的方法**获取主对象**模块。在这里您可以看到示例代码。

**红宝石代码**

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
## **Aspose.Diagram - 按名称获取主对象**
要按名称获取主对象，请使用**Aspose.Diagram Java 红宝石**， 称呼**get_master_object_by_name**的方法**获取主对象**模块。在这里您可以看到示例代码。

**红宝石代码**

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
## **下载运行代码**
下载**从绘图中获取主对象 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/getmasterobject.rb)
