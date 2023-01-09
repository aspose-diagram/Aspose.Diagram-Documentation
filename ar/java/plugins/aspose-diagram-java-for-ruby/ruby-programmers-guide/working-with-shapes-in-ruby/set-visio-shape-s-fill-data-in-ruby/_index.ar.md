---
title: تعيين Visio بيانات تعبئة الشكل في روبي
type: docs
weight: 130
url: /ar/java/set-visio-shape-s-fill-data-in-ruby/
---
## **Aspose.Diagram - تعيين Visio بيانات تعبئة الشكل**
 لتعيين Visio بيانات تعبئة الشكل باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**SetShapeFillData** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 بيانات_dir = File.dirname (File.dirname (File.dirname (File.dirname (__ملف__)))) + '/ بيانات /'

\ # إنشاء مثيل Diagram

diagram = Rjb :: import ('com.aspose.diagram.Diagram'). new (data_dir + "Drawing.vsd")

الأشكال = diagram.getPages (). getPage (0) .getShapes ()

أنا = 0

 عندما أنا< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "rectangle" && shape.getID() == 1

        shape.getFill().getFillBkgnd().setValue(diagram.getPages().getPage(0).getShapes().getShape(0).getFill().getFillBkgnd().getValue())

        shape.getFill().getFillForegnd().setValue("#ebf8df")

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "SetShapeFillData.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Set visio shape's fill data."

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**ضبط Visio بيانات تعبئة الشكل (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/setshapefilldata.rb)
