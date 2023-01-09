---
title: تحقق من وجود ماجستير في رسم Visio بلون الياقوت
type: docs
weight: 10
url: /ar/java/check-presence-of-a-master-in-the-visio-drawing-in-ruby/
---
## **Aspose.Diagram - التحقق من وجود رئيسي بواسطة المعرف**
 للتحقق من وجود رئيسي عن طريق المعرف باستخدام**Aspose.Diagram Java لروبي** ، مكالمة**check_presence_master_by_id** طريقة**CheckPresenceOfMaster** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

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
## **Aspose.Diagram - التحقق من وجود رئيسي بالاسم**
 للتحقق من وجود رئيسي بالاسم باستخدام**Aspose.Diagram Java لروبي** ، مكالمة**check_presence_master_by_name** طريقة**CheckPresenceOfMaster** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

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
## **قم بتنزيل كود التشغيل**
 تحميل**تحقق من وجود ماجستير في رسم Visio (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/checkpresenceofmaster.rb)
