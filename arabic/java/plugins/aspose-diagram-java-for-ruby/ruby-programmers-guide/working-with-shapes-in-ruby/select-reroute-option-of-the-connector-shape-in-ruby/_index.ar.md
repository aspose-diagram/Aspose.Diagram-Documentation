---
title: حدد خيار إعادة التوجيه لشكل الموصل في روبي
type: docs
weight: 90
url: /ar/java/select-reroute-option-of-the-connector-shape-in-ruby/
---
## **Aspose.Diagram - حدد خيار إعادة التوجيه لشكل الموصل**
 لتحديد خيار إعادة التوجيه لشكل الموصل باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**حدد خيار إعادة التوجيه** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Access a particular page

page = diagram.getPages().getPage("Flow 1")

\# get a particular connector shape

shape = page.getShapes().getShape(1)

\# set reroute option

shape.getLayout().getConFixedCode().setValue(Rjb::import('com.aspose.diagram.ConFixedCodeValue').NEVER_REROUTE)

\# Save diagram

diagram.save(data_dir + "SelectRerouteOption.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Seleted reroute option of the connector shape."

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**حدد خيار إعادة التوجيه لشكل الموصل (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/selectrerouteoption.rb)
