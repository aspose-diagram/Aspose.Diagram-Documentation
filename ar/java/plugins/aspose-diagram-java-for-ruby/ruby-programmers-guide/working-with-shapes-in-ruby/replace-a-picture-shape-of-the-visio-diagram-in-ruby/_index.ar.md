---
title: استبدال شكل صورة Visio Diagram في روبي
type: docs
weight: 60
url: /ar/java/replace-a-picture-shape-of-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - استبدال شكل صورة Visio Diagram**
 لاستبدال شكل صورة Visio Diagram باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**استبدل الصورة** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 بيانات_dir = File.dirname (File.dirname (File.dirname (File.dirname (__ملف__)))) + '/ بيانات /'

\ # إنشاء مثيل Diagram

diagram = Rjb :: import ('com.aspose.diagram.Diagram'). new (data_dir + "Drawing.vsd")

\ # تحويل الصورة إلى مصفوفة بايت

fi = Rjb :: import ('java.io.File'). new (data_dir + "star.png")

file_content = Rjb :: import ('java.nio.file.Files'). readAllBytes (fi.toPath ())

الأشكال = diagram.getPages (). getPage ("التدفق 1"). getShapes ()

أنا = 0

 عندما أنا< shapes.getCount()

    shape = shapes.get(i)

    # Filter shapes by type Foreign

    if shape.getType() == Rjb::import('com.aspose.diagram.TypeValue').FOREIGN

        # replace picture shape

        shape.getForeignData().setValue(file_content)

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "ReplacePictureShape.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Replaced picture shape successfully!"

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**استبدال شكل صورة Visio Diagram (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/replacepictureshape.rb)
