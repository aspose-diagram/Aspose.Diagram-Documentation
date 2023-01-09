---
title: قم بإنشاء خلية معرّفة من قبل المستخدم في ورقة الشكل في روبي
type: docs
weight: 10
url: /ar/java/create-user-defined-cell-in-the-shapesheet-in-ruby/
---
## **Aspose.Diagram - تكوين خلية معرّفة من قبل المستخدم في ورقة الشكل**
 لإنشاء خلية معرّفة من قبل المستخدم في ورقة الشكل باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**CreateUserDefinedCell** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 بيانات_dir = File.dirname (File.dirname (File.dirname (File.dirname (__ملف__)))) + '/ بيانات /'

\ # إنشاء مثيل Diagram

diagram = Rjb :: import ('com.aspose.diagram.Diagram'). new (data_dir + "Drawing.vsd")

الصفحات = diagram.getPages ()

أنا = 0

 عندما أنا< pages.getCount()

    page = pages.get(i)

    shapes = page.getShapes()

    j = 0

    while j < shapes.getCount()

        shape = shapes.get(j)

        if shape.getNameU() == "Process"

            # Initialize user object

            user = Rjb::import('com.aspose.diagram.User').new

            user.setName("UserDefineCell")

            user.getValue().setVal("800")

            # Add user-defined cell

            shape.getUsers().add(user)

        end

        j +=1

    end

    i +=1

end

\# Save diagram

diagram.save(data_dir + "UserDefinedCells.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

puts "Created User-defined Cell in the ShapeSheet."

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**تكوين خلية معرّفة من قبل المستخدم في ورقة الشكل (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/UserDefinedCells/createuserdefinedcell.rb)
