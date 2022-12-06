---
title: استرجع Visio معلومات الشكل في PHP
type: docs
weight: 70
url: /ar/java/retrieve-visio-shape-information-in-php/
---
## **Aspose.Diagram - استرجاع Visio معلومات الشكل**
 لاسترداد معلومات الشكل Visio باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**GetShapeInfo** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing1.vsd");

$shapes = $diagram->getPages()->getPage(0)->getShapes();

$i = 0;

while ($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

\# Display information about the shapes

print "Shape ID : " . (string)$shape->getID().PHP_EOL;

print "Name : " . (string)$shape->getName().PHP_EOL;

print "Master Shape : ".(string)$shape->getMaster()->getName().PHP_EOL;

$i += 1;

}

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**استرجاع Visio معلومات الشكل (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/GetShapeInfo.php)
