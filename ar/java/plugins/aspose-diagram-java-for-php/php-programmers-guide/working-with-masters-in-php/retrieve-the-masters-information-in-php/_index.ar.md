---
title: استرجع معلومات الماجستير في PHP
type: docs
weight: 30
url: /ar/java/retrieve-the-masters-information-in-php/
---
## **Aspose.Diagram - استرجاع معلومات الماجستير**
 لاسترداد معلومات الماجستير باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**GetMasterInfo** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir . "drawing.vsd");

$masters = $diagram->getMasters();

$i = 0;

while ($i<sizeof($masters->getCount())){

$master = $masters->get($i);

print "Master ID : " . (string)$master->getID().PHP_EOL;

print "Master Name : " . (string)$master->getName().PHP_EOL;

$i += 1;

}

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**استرجاع معلومات الماجستير (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/GetMasterInfo.php)
