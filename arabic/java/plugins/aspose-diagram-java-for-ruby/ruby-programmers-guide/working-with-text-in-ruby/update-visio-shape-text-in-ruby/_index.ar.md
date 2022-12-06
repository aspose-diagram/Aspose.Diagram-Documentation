---
title: تحديث Visio Shape Text in Ruby
type: docs
weight: 30
url: /ar/java/update-visio-shape-text-in-ruby/
---
## **Aspose.Diagram - تحديث Visio شكل النص**
لتحديث Visio شكل نص باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**UpdateShapeText** وحدة. هنا يمكنك أن ترى رمز المثال.

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

        shape.getText().getValue().clear()

        shape.getText().getValue().add(Rjb::import('com.aspose.diagram.Txt').new("New Text"))

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "UpdateShapeText.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Updated shape text."

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**تحديث Visio شكل النص (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Text/updateshapetext.rb)
