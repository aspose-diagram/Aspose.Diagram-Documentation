---
title: استرجع Visio معلومات الصفحة في روبي
type: docs
weight: 30
url: /ar/java/retrieve-visio-page-information-in-ruby/
---
## **Aspose.Diagram - استرجاع Visio معلومات الصفحة**
 لاسترداد معلومات الصفحة Visio باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**GetPageInfo** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

# page = diagram.getPages().getPage(page_id)

page = diagram.getPages().getPage(0)

puts "Page ID : " + page.getName().to_s

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**استرداد Visio معلومات الصفحة (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/getpageinfo.rb)
