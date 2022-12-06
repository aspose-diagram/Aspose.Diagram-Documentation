---
title: استرجع معلومات الموصلات Visio في PHP
type: docs
weight: 50
url: /ar/java/retrieve-visio-connectors-information-in-php/
---
## **Aspose.Diagram - استرجاع معلومات الموصلات Visio**
 لاسترداد معلومات الموصلات Visio باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**GetConnectorsInfo** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$connectors = $diagram->getPages()->getPage(0)->getConnects();

$i = 0;

while ($i<sizeof($connectors->getCount())) {

$connector =$connectors->get($i);

\# Display information about the Connectors

print "From Shape ID : ".(string)$connector->getFromSheet().PHP_EOL;

print "To Shape ID : ".(string)$connector->getToSheet().PHP_EOL;

$i+=1;

}

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**استرداد معلومات الموصلات Visio (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/GetConnectorsInfo.php)
