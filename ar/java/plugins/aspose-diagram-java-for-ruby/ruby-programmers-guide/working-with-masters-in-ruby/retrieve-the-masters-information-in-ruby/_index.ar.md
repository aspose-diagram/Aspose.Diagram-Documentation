---
title: استرجع معلومات الماجستير في روبي
type: docs
weight: 30
url: /ar/java/retrieve-the-masters-information-in-ruby/
---
## **Aspose.Diagram - استرجاع معلومات الماجستير**
 لاسترداد معلومات الماجستير باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**GetMasterInfo** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 بيانات_dir = File.dirname (File.dirname (File.dirname (File.dirname (__ملف__)))) + '/ بيانات /'

\ # اتصل بالمنشئ diagram لتحميل diagram من ملف VSD

diagram = Rjb :: import ('com.aspose.diagram.Diagram'). new (data_dir + "Drawing.vsd")

الماجستير = diagram.getMasters ()

أنا = 0

 عندما أنا< masters.getCount()

    master = masters.get(i)

    puts "Master ID : " + master.getID().to_s

    puts "Master Name : " + master.getName().to_s

    i +=1

end

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**استرجاع معلومات الماجستير (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Masters/getmasterinfo.rb)
