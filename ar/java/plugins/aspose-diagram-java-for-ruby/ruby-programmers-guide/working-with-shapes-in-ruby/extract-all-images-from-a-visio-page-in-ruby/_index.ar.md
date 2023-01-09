---
title: استخراج كافة الصور من صفحة Visio في روبي
type: docs
weight: 30
url: /ar/java/extract-all-images-from-a-visio-page-in-ruby/
---
## **Aspose.Diagram - استخراج كافة الصور من صفحة Visio**
 لاستخراج كافة الصور من صفحة Visio باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**استخراج الصور** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 بيانات_dir = File.dirname (File.dirname (File.dirname (File.dirname (__ملف__)))) + '/ بيانات /'

\ # إنشاء مثيل Diagram

diagram = Rjb :: import ('com.aspose.diagram.Diagram'). new (data_dir + "Drawing.vsd")

الأشكال = diagram.getPages (). getPage ("التدفق 1"). getShapes ()

أنا = 0

 عندما أنا< shapes.getCount()

    shape = shapes.get(i)

    # Filter shapes by type Foreign

    if shape.getType() == Rjb::import('com.aspose.diagram.TypeValue').FOREIGN

        # create an image file

        fos = Rjb::import('java.io.FileOutputStream').new(data_dir + "Image#{i}.bmp")

        fos.write(shape.getForeignData().getValue())

        fos.close()

    end

    i +=1

end

puts "Extracted images successfully!"

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**استخراج كافة الصور من صفحة Visio (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/extractimages.rb)
