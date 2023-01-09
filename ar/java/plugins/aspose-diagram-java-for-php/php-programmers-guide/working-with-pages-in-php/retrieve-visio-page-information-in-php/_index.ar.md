---
title: استرجع Visio معلومات الصفحة في PHP
type: docs
weight: 30
url: /ar/java/retrieve-visio-page-information-in-php/
---
## **Aspose.Diagram - استرجاع Visio معلومات الصفحة**
 لاسترداد معلومات الصفحة Visio باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**GetPageInfo** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

# page = diagram.getPages().getPage(page_id)

$page = $diagram->getPages()->getPage(0);

print "Page ID : ".$page->getName().PHP_EOL;

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**استرداد Visio معلومات الصفحة (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/GetPageInfo.php)
