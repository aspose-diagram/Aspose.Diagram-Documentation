---
title: احصل على كائن صفحة من Visio رسم في ياقوت
type: docs
weight: 10
url: /ar/java/get-a-page-object-from-visio-drawing-in-ruby/
---
## **Aspose.Diagram - الحصول على كائن صفحة بواسطة المعرف**
 للحصول على كائن صفحة عن طريق المعرف باستخدام**Aspose.Diagram Java لروبي** ، مكالمة**get_page_object_by_id** طريقة**GetPageObject** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 def get_page_object_by_id() 

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    page_id = 0

    # Get page object by id

    page = diagram.getPages().getPage(page_id)

    puts "Page : " + page.to_string

end

{{< /highlight >}}
## **Aspose.Diagram - الحصول على كائن صفحة بالاسم**
 للحصول على كائن صفحة بالاسم باستخدام**Aspose.Diagram Java لروبي** ، مكالمة**get_page_object_by_name** طريقة**GetPageObject** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 def get_page_object_by_name() 

    data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

    # Call the diagram constructor to load diagram from a VSD file

    diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

    # Set page name

    page_name = "Flow 1"

    # Get page object by name

    page = diagram.getPages().getPage(page_name)

    puts "Page : " + page.to_string

end

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**الحصول على كائن صفحة من رسم Visio (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/getpageobject.rb)
