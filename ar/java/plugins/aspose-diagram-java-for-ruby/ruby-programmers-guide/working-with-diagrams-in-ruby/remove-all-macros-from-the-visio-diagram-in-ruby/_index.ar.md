---
title: قم بإزالة كافة وحدات الماكرو من Visio Diagram في روبي
type: docs
weight: 50
url: /ar/java/remove-all-macros-from-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - إزالة كافة وحدات الماكرو من Visio Diagram**
 لإزالة كافة وحدات الماكرو من Visio Diagram باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**RemoveAllMacrosFromDiagram** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# remove all macros

diagram.setVbProjectData(nil)

\# Save as VDX

diagram.save(data_dir + "RemoveAllMacros.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Removed all macros from diagram successfully!"

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**قم بإزالة كافة وحدات الماكرو من Visio Diagram (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/removeallmacrosfromdiagram.rb)
