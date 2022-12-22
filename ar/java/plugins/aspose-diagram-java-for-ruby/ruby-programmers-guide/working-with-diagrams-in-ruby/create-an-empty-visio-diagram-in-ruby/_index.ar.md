---
title: قم بإنشاء Visio Diagram فارغًا في روبي
type: docs
weight: 10
url: /ar/java/create-an-empty-visio-diagram-in-ruby/
---
## **Aspose.Diagram - أنشئ Visio Diagram فارغًا**
 لإنشاء Visio Diagram فارغ باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**إنشاء رسم بياني** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new

\# Save as VDX

diagram.save(data_dir + "CreateDiagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Created visio diagram successfully!"

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**إنشاء Visio Diagram (Aspose.Diagram) فارغ**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/creatediagram.rb)
