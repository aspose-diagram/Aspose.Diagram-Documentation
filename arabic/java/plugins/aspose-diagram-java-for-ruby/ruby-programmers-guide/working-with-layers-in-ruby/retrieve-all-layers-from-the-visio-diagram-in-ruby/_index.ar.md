---
title: استرجع كل الطبقات من Visio Diagram في روبي
type: docs
weight: 30
url: /ar/java/retrieve-all-layers-from-the-visio-diagram-in-ruby/
---
## **Aspose.Diagram - استرجاع كل الطبقات**
 لاسترداد جميع الطبقات باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**GetAllLayers** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 بيانات_dir = File.dirname (File.dirname (File.dirname (File.dirname (__ملف__)))) + '/ بيانات /'

\ # إنشاء مثيل Diagram

diagram = Rjb :: import ('com.aspose.diagram.Diagram'). new (data_dir + "Drawing.vsd")

\ # الحصول على Visio صفحة

page = diagram.getPages (). getPage (0)

الطبقات = page.getPageSheet (). getLayers ()

أنا = 0

 عندما أنا< layers.getCount()

    layer = layers.get(i)

    puts "Name: " + layer.getName().getValue().to_s

    puts "Visibility: " + layer.getVisible().getValue().to_s

    puts "Status: " + layer.getStatus().getValue().to_s



    i +=1

end

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**استرداد كافة الطبقات من Visio Diagram (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Layers/getalllayers.rb)
