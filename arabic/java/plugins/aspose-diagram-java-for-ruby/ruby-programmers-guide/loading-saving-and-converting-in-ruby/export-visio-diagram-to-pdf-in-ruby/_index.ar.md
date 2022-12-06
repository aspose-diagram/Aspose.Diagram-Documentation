---
title: تصدير Visio Diagram إلى PDF في روبي
type: docs
weight: 40
url: /ar/java/export-visio-diagram-to-pdf-in-ruby/
---
## **Aspose.Diagram - تصدير Visio Diagram إلى PDF**
 لتصدير Visio Diagram إلى PDF باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**ExportToPdf** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Save as PDF file format

diagram.save(data_dir + "Diagram.pdf", Rjb::import('com.aspose.diagram.SaveFileFormat').PDF)

puts "Exported visio diagram to pdf."

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
تحميل**تصدير Visio Diagram إلى PDF (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Export/exporttopdf.rb)
