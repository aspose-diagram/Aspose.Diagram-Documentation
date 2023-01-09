---
title: ضبط Visio بيانات XForm للشكل في روبي
type: docs
weight: 150
url: /ar/java/set-visio-shape-s-xform-data-in-ruby/
---
## **Aspose.Diagram تعيين Visio بيانات XForm للشكل**
 لتعيين Visio بيانات XForm للشكل باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**SetShapeXFormData** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 بيانات_dir = File.dirname (File.dirname (File.dirname (File.dirname (__ملف__)))) + '/ بيانات /'

\ # إنشاء مثيل Diagram

diagram = Rjb :: import ('com.aspose.diagram.Diagram'). new (data_dir + "Drawing.vsd")

الأشكال = diagram.getPages (). getPage (0) .getShapes ()

أنا = 0

 عندما أنا< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "process" && shape.getID() == 1

        shape.getXForm().getPinX().setValue(5)

        shape.getXForm().getPinY().setValue(5)

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "SetShapeXFormData.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set visio shape's XForm data."

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**ضبط Visio بيانات XForm للشكل (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapexformdata.rb)
