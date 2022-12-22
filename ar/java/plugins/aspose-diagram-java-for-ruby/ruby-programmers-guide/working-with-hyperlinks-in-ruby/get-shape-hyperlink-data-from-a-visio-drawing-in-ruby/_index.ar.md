---
title: احصل على بيانات الارتباط التشعبي للشكل من رسم Visio في ياقوت
type: docs
weight: 20
url: /ar/java/get-shape-hyperlink-data-from-a-visio-drawing-in-ruby/
---
## **Aspose.Diagram - الحصول على بيانات الارتباط التشعبي للشكل**
للحصول على بيانات الارتباط التشعبي بالشكل باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**GetShapeHyperlinkData** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 بيانات_dir = File.dirname (File.dirname (File.dirname (File.dirname (__ملف__)))) + '/ بيانات /'

\ # إنشاء مثيل Diagram

diagram = Rjb :: import ('com.aspose.diagram.Diagram'). new (data_dir + "Hyperlinks.vdx")

\ # الحصول على شكل معين

الشكل = diagram.getPages (). getPage ("Flow 1"). getShapes (). getShape (1)

الارتباطات التشعبية = shape.getHyperlinks ()

أنا = 0

 عندما أنا< hyperlinks.getCount()

    hyperlink = hyperlinks.get(i)

    puts "Address: " + hyperlink.getAddress().getValue().to_s

    puts "Sub Address: " + hyperlink.getSubAddress().getValue().to_s

    puts "Description: " + hyperlink.getDescription().getValue().to_s

    i +=1

end

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**الحصول على بيانات الارتباط التشعبي للشكل من رسم Visio (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Hyperlinks/getshapehyperlinkdata.rb)
