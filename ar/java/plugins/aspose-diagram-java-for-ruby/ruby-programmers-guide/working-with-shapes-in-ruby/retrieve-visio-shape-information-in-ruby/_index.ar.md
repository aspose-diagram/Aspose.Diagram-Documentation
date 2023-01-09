---
title: استرجع Visio معلومات الشكل في ياقوت
type: docs
weight: 70
url: /ar/java/retrieve-visio-shape-information-in-ruby/
---
## **Aspose.Diagram - استرجاع Visio معلومات الشكل**
 لاسترداد معلومات الشكل Visio باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**GetShapeInfo** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 بيانات_dir = File.dirname (File.dirname (File.dirname (File.dirname (__ملف__)))) + '/ بيانات /'

\ # إنشاء مثيل Diagram

diagram = Rjb :: import ('com.aspose.diagram.Diagram'). new (data_dir + "Drawing.vsd")

الأشكال = diagram.getPages (). getPage (0) .getShapes ()

أنا = 0

 عندما أنا< shapes.getCount()

    shape = shapes.get(i)

    # Display information about the shapes

    puts "Shape ID : " + shape.getID().to_s

    puts "Name : " + shape.getName().to_s

    puts "Master Shape : " + shape.getMaster().getName().to_s

    i +=1

end

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**استرجاع Visio معلومات الشكل (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/getshapeinfo.rb)
