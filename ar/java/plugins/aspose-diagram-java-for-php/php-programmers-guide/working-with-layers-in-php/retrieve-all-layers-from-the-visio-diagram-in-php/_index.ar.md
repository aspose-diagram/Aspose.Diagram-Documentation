---
title: استرجع كل الطبقات من Visio Diagram في PHP
type: docs
weight: 20
url: /ar/java/retrieve-all-layers-from-the-visio-diagram-in-php/
---
## **Aspose.Diagram - استرجاع كل الطبقات**
 لاسترداد جميع الطبقات باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**GetAllLayers** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "Drawing.vsd");

\# get Visio page

$page=$diagram->getPages()->getPage(0);

$layers=$page->getPageSheet()->getLayers();

$i = 0;

while ($i<(int)(string)$layers->getCount()) {

$layer=$layers->get($i);

print "Name: " . (string)$layer->getName()->getValue();

print "Visibility: " . (string)$layer->getVisible()->getValue();

print "Status: " . (string)$layer->getStatus()->getValue();

$i += 1;

}

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**استرداد كافة الطبقات من Visio Diagram (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithLayers/GetAllLayers.php)
