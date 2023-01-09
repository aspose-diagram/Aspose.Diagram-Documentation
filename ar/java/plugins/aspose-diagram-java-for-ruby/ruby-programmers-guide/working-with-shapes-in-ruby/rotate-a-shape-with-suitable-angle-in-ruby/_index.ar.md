---
title: قم بتدوير شكل بزاوية مناسبة باللون الياقوتي
type: docs
weight: 80
url: /ar/java/rotate-a-shape-with-suitable-angle-in-ruby/
---
## **Aspose.Diagram - قم بتدوير شكل بزاوية مناسبة**
 لتدوير شكل بزاوية مناسبة باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**استدارة** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Create instance of Diagram

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

\# Add a shape and set the angle

diagram.getPages().getPage(0).getShapes().getShape(1).setAngle(190)

\# Save diagram

diagram.save(data_dir + "RotateShape.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Rotated shape."

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**تدوير شكل بزاوية مناسبة (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/rotateshape.rb)
