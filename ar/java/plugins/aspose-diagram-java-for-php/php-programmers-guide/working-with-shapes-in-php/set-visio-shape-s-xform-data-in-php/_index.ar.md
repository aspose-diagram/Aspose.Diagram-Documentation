---
title: قم بتعيين Visio بيانات XForm للشكل في PHP
type: docs
weight: 150
url: /ar/java/set-visio-shape-s-xform-data-in-php/
---
## **Aspose.Diagram تعيين Visio بيانات XForm للشكل**
 لتعيين Visio بيانات XForm للشكل باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**SetShapeXFormData** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes = $diagram->getPages()->getPage(0)->getShapes();

$i=0;

while ($i<(int)(string)$shapes->getCount()){

$shape = $shapes->get($i);

if ($shape->getNameU()=="process" && $shape->getID() == 1) {

$shape->getXForm()->getPinX()->setValue(5);

$shape->getXForm()->getPinY()->setValue(5);

}

$i+= 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SetShapeXFormData.vdx",$saveFileFormat->VDX);

print "Set visio shape's XForm data.".PHP_EOL;

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**ضبط Visio بيانات XForm للشكل (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeXFormData.php)
