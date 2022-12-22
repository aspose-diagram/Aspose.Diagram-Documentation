---
title: أضف ارتباطًا تشعبيًا إلى شكل Visio بلون روبي
type: docs
weight: 10
url: /ar/java/add-hyperlink-to-a-visio-shape-in-ruby/
---
## **Aspose.Diagram - إضافة ارتباط تشعبي**
 لإضافة ارتباط تشعبي باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**إضافة ارتباط تشعبي إلى شكل** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Initialize Hyperlink object

hyperlink = Rjb::import('com.aspose.diagram.Hyperlink').new

\# Set address value

hyperlink.getAddress().setValue("http://www.google.com/")

\# Set sub address value

hyperlink.getSubAddress().setValue("Sub address here")

\# Set description value

hyperlink.getDescription().setValue("Description here")

\# Set name

hyperlink.setName("MyHyperLink")

\# Add hyperlink to the shape

diagram.getPages().getPage("Flow 1").getShapes().getShape(1).getHyperlinks().add(hyperlink)

\# Save diagram

diagram.save(data_dir + "Hyperlinks.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Added hyperlik to shape successfully!"

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**إضافة ارتباط تشعبي إلى شكل Visio (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Hyperlinks/addhyperlinktoshape.rb)
