---
title: استرجع معلومات الموصلات Visio في روبي
type: docs
weight: 20
url: /ar/java/retrieve-visio-connectors-information-in-ruby/
---
## **Aspose.Diagram - استرجاع معلومات الموصلات Visio**
 لاسترداد معلومات الموصلات Visio باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**GetConnectorsInfo** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 بيانات_dir = File.dirname (File.dirname (File.dirname (File.dirname (__ملف__)))) + '/ بيانات /'

\ # إنشاء مثيل Diagram

diagram = Rjb :: import ('com.aspose.diagram.Diagram'). new (data_dir + "Drawing.vsd")

الموصلات = diagram.getPages (). getPage (0) .getConnects ()

أنا = 0

 عندما أنا< connectors.getCount()

    connector = connectors.get(i)

    # Display information about the Connectors

    puts "From Shape ID : " + connector.getFromSheet().to_s

    puts "To Shape ID : " + connector.getToSheet().to_s

    i +=1

end

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**استرداد معلومات الموصلات Visio (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Diagrams/getconnectorsinfo.rb)

