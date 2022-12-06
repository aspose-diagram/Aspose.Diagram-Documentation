---
title: اقرأ الخلايا المحددة بواسطة المستخدم في Ruby
type: docs
weight: 20
url: /ar/java/read-shape-s-user-defined-cells-in-ruby/
---
## **Aspose.Diagram - اقرأ الخلايا المعرفة بواسطة المستخدم للشكل**
 لقراءة الخلايا المحددة بواسطة المستخدم الخاصة بالشكل باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**ReadUserDefinedCells** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 بيانات_dir = File.dirname (File.dirname (File.dirname (File.dirname (__ملف__)))) + '/ بيانات /'

\ # إنشاء مثيل Diagram

diagram = Rjb :: import ('com.aspose.diagram.Diagram'). new (data_dir + "UserDefinedCells.vdx")

الأشكال = diagram.getPages (). getPage ("التدفق 1"). getShapes ()

أنا = 0

 عندما أنا< shapes.getCount()

    shape = shapes.get(i)

    if shape.getNameU() == "Process"

        users = shape.getUsers()

        j = 0

        while j < users.getCount()

            user = users.get(j)

            puts user.getName() + ": " + user.getValue().getVal()

            j +=1

        end

        break

    end

    i +=1

end

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**قراءة الخلايا المحددة بواسطة المستخدم الخاصة بالشكل (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/readuserdefinedcells.rb)
