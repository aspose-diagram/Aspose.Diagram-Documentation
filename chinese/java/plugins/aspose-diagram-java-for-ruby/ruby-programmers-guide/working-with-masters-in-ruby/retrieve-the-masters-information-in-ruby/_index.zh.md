---
title: 在 Ruby 中检索大师信息
type: docs
weight: 30
url: /zh/java/retrieve-the-masters-information-in-ruby/
---
## **Aspose.Diagram - 检索大师信息**
使用检索大师信息**Aspose.Diagram Java 红宝石** 只需调用**获取MasterInfo**模块。在这里您可以看到示例代码。

**红宝石代码**

{{< highlight "ruby" >}}

数据_dir = File.dirname(File.dirname(File.dirname(File.dirname(__文件__)))) + '/数据/'

\#调用diagram构造函数从VSD文件中加载diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

大师 = diagram.getMasters()

我 = 0

当我< masters.getCount()

    master = masters.get(i)

    puts "Master ID : " + master.getID().to_s

    puts "Master Name : " + master.getName().to_s

    i +=1

end

{{< /highlight >}}
## **下载运行代码**
下载**检索大师信息 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/getmasterinfo.rb)
