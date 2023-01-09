---
title: اضبط ارتفاع الشكل وعرضه في روبي
type: docs
weight: 120
url: /ar/java/set-the-height-and-width-of-a-shape-in-ruby/
---
## **Aspose.Diagram - ضبط ارتفاع الشكل وعرضه**
 لتعيين ارتفاع الشكل وعرضه باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**SetShapeHeightAndWidth** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 بيانات_dir = File.dirname (File.dirname (File.dirname (File.dirname (__ملف__)))) + '/ بيانات /'

\ # إنشاء مثيل Diagram

diagram = Rjb :: import ('com.aspose.diagram.Diagram'). new (data_dir + "Drawing.vsd")

الأشكال = diagram.getPages (). getPage (0) .getShapes ()

أنا = 0

 عندما أنا< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process" && shape.getID() == 1

        shape.setWidth(2 * shape.getXForm().getWidth().getValue())

        shape.setHeight(2 * shape.getXForm().getHeight().getValue())

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "SetShapeHeightAndWidth.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set height and width of shape."

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**ضبط ارتفاع الشكل وعرضه (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapeheightandwidth.rb)
