---
title: تصدير Visio Diagram إلى XPS في روبي
type: docs
weight: 80
url: /ar/java/export-visio-diagram-to-xps-in-ruby/
---
## **Aspose.Diagram - تصدير Visio Diagram إلى XPS**
 لتصدير Visio Diagram إلى XPS باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**ExportToXps** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as XPS

diagram.save(data_dir + "Diagram.xps", Rjb::import('com.aspose.diagram.SaveFileFormat').XPS)

puts "Exported visio diagram to XPS."

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**تصدير Visio Diagram إلى XPS (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttoxps.rb)
