---
title: اقرأ Visio بيانات الشكل في روبي
type: docs
weight: 50
url: /ar/java/read-visio-shape-data-in-ruby/
---
## **Aspose.Diagram - اقرأ كافة خصائص الشكل**
 لقراءة كافة خصائص الشكل باستخدام**Aspose.Diagram Java لروبي** ، مكالمة**read_all_shape_properties** طريقة**قراءة بيانات الشكل** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 قراءة مواطنه_الكل_الشكل_الخصائص ()

 بيانات_dir = File.dirname (File.dirname (File.dirname (File.dirname (__ملف__)))) + '/ بيانات /'

 # إنشاء مثيل Diagram

 diagram = Rjb :: import ('com.aspose.diagram.Diagram'). new (data_dir + "Drawing.vsd")

 الأشكال = diagram.getPages (). getPage (0) .getShapes ()



 أنا = 0

 عندما أنا< shapes.getCount()

        shape = shapes.get(i)

        if shape.getName() == "Process"

            j = 0

            while j < shape.getProps().getCount()

                property = shape.getProps().get(j)

                puts property.getLabel().getValue() + ": " + property.getValue().getVal()

                j +=1

            end

            break

        end

        i +=1

    end

end

{{< /highlight >}}
## **Aspose.Diagram - اقرأ خاصية الشكل بالاسم**
 لقراءة خاصية الشكل بالاسم باستخدام**Aspose.Diagram Java لروبي** ، مكالمة**read_shape_property_by_name** طريقة**قراءة بيانات الشكل** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 قراءة مواطنه_شكل_منشأه_بواسطة_اسم()

 بيانات_dir = File.dirname (File.dirname (File.dirname (File.dirname (__ملف__)))) + '/ بيانات /'

 # إنشاء مثيل Diagram

 diagram = Rjb :: import ('com.aspose.diagram.Diagram'). new (data_dir + "Drawing.vsd")

 الأشكال = diagram.getPages (). getPage (0) .getShapes ()



 أنا = 0

 عندما أنا< shapes.getCount()

        shape = shapes.get(i)

        if shape.getName() == "Process"

            property = shape.getProps().getProp("Cost")

            puts property.getLabel().getValue() + ": " + property.getValue().getVal()

        end

        i +=1

    end

end

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**قراءة Visio بيانات الشكل (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Shapes/readshapedata.rb)
