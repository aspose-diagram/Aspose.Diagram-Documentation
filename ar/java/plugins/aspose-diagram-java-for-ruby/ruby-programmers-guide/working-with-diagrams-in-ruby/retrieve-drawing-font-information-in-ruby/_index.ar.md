---
title: استرجع معلومات خط الرسم في روبي
type: docs
weight: 30
url: /ar/java/retrieve-drawing-font-information-in-ruby/
---
## **Aspose.Diagram - استرجاع معلومات خط الرسم**
 لاسترداد معلومات خط الرسم باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**GetDiagramFontInfo** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 بيانات_dir = File.dirname (File.dirname (File.dirname (File.dirname (__ملف__)))) + '/ بيانات /'

\ # إنشاء مثيل Diagram

diagram = Rjb :: import ('com.aspose.diagram.Diagram'). new (data_dir + "Drawing.vsd")

الخطوط = diagram.getFonts ()

أنا = 0

 عندما أنا< fonts.getCount()

    font = fonts.get(i)

    # Display information about the fonts

    puts font.getName()

    i +=1

end

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**استرداد معلومات خط الرسم (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/getdiagramfontinfo.rb)
