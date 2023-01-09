---
title: احصل على بيانات الارتباط التشعبي للشكل من رسم Visio في PHP
type: docs
weight: 20
url: /ar/java/get-shape-hyperlink-data-from-a-visio-drawing-in-php/
---
## **Aspose.Diagram - الحصول على بيانات الارتباط التشعبي للشكل**
للحصول على بيانات الارتباط التشعبي بالشكل باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**GetShapeHyperlinkData** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "drawing.vdx");

\# Get a particular shape

$shape=$diagram->getPages()->getPage("Flow 1")->getShapes()->getShape(1);

$hyperlinks=$shape->getHyperlinks();

$i=0;

while ($i<(int)(string)$hyperlinks->getCount()) {

$hyperlink=$hyperlinks->get($i);

print "Address: " . (string)$hyperlink->getAddress()->getValue();

print "Sub Address: " . (string)$hyperlink->getSubAddress()->getValue();

print "Description: " . (string)$hyperlink->getDescription()->getValue();

$i+=1;

}

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**الحصول على بيانات الارتباط التشعبي للشكل من رسم Visio (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithHyperlinks/GetShapeHyperlinkData.php)
