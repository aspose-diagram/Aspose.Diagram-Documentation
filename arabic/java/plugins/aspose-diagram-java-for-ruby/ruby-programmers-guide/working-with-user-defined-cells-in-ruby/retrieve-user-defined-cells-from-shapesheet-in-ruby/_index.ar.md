---
title: استرجع الخلايا المعرفة من قبل المستخدم من ورقة الأشكال في روبي
type: docs
weight: 30
url: /ar/java/retrieve-user-defined-cells-from-shapesheet-in-ruby/
---
## **Aspose.Diagram - استرداد الخلايا المعرفة من قبل المستخدم من ورقة الأشكال**
 لاسترداد الخلايا المعرفة من قبل المستخدم من الأشكال باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**GetUserDefinedCells** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 بيانات_dir = File.dirname (File.dirname (File.dirname (File.dirname (__ملف__)))) + '/ بيانات /'

\ # إنشاء مثيل Diagram

diagram = Rjb :: import ('com.aspose.diagram.Diagram'). new (data_dir + "UserDefinedCells.vdx")

الصفحات = diagram.getPages ()

العد = 0

 أثناء العد< pages.getCount()

    page = pages.get(count)

    shapes = page.getShapes()

    i = 0

    while i < shapes.getCount()

        shape = shapes.get(i)

        if shape.getNameU() == "Process"

            users = shape.getUsers()

            j = 0

            while j < users.getCount()

                user = users.get(j)

                            puts "Name: " + user.getNameU() + " Value: " + user.getValue().getVal() + " Prompt: " + user.getPrompt().getValue()

                j +=1

            end

            break

        end

        i +=1

    end

    count +=1

end

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**استرجاع الخلايا المعرفة من قبل المستخدم من ورقة الأشكال (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/getuserdefinedcells.rb)
