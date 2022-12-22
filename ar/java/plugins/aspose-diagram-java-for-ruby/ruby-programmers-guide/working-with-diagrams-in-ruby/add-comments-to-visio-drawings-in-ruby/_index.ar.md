---
title: أضف تعليقات إلى Visio رسومات روبي
type: docs
weight: 40
url: /ar/java/add-comments-to-visio-drawings-in-ruby/
---
## **Aspose.Diagram - إضافة تعليقات إلى رسومات Visio**
 لإضافة تعليقات إلى Visio الرسومات باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**AddCommentToDiagram** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Add comment

diagram.getPages().getPage(0).addComment(7.205905511811023, 3.880708661417323, "test@")

\# Save as VDX

diagram.save(data_dir + "AddComment.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Added comment successfully!"

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**أضف تعليقات إلى رسومات Visio (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/addcommenttodiagram.rb)
