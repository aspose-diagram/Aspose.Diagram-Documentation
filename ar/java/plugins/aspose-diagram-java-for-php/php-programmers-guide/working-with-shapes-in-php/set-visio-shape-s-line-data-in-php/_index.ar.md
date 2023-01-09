---
title: قم بتعيين Visio بيانات خط الشكل في PHP
type: docs
weight: 140
url: /ar/java/set-visio-shape-s-line-data-in-php/
---
## **Aspose.Diagram - تعيين Visio بيانات خط الشكل**
 لتعيين Visio بيانات خط الشكل باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**SetShapeLineData** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes = $diagram->getPages()->getPage(0)->getShapes();

$i=0;

while ($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

if ($shape->getNameU() == "rectangle" && (int)(string)$shape->getID() == 1) {

$shape->getLine()->getLineColor()->setValue($diagram->getPages()->getPage(0)->getShapes()->getShape(1)->getFill()->getFillForegnd()->getValue());

$shape->getLine()->getLineWeight()->setValue(0.07041666666666667);

$shape->getLine()->getRounding()->setValue(0.1);

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SetShapeLineData.vdx", $saveFileFormat->VDX);

print "Set visio shape's line data.".PHP_EOL;

}

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**ضبط Visio بيانات خط الشكل (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeLineData.php)
