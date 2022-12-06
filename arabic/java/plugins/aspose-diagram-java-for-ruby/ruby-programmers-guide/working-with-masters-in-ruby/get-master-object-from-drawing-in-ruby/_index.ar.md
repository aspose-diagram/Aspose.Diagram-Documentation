---
title: احصل على كائن رئيسي من الرسم في روبي
type: docs
weight: 20
url: /ar/java/get-master-object-from-drawing-in-ruby/
---
## **Aspose.Diagram - الحصول على كائن رئيسي بواسطة المعرف**
 للحصول على كائن رئيسي عن طريق المعرف باستخدام**Aspose.Diagram Java لروبي** ، مكالمة**get_master_object_by_id** طريقة**GetMasterObject** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

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
## **Aspose.Diagram - الحصول على كائن رئيسي بالاسم**
 للحصول على كائن رئيسي بالاسم باستخدام**Aspose.Diagram Java لروبي** ، مكالمة**get_master_object_by_name** طريقة**GetMasterObject** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

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
## **قم بتنزيل كود التشغيل**
 تحميل**الحصول على كائن رئيسي من الرسم (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/getmasterobject.rb)
