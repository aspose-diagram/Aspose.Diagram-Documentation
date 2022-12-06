---
title: قم بتعيين Visio بيانات تعبئة الشكل في PHP
type: docs
weight: 130
url: /ar/java/set-visio-shape-s-fill-data-in-php/
---
## **Aspose.Diagram - تعيين Visio بيانات تعبئة الشكل**
 لتعيين Visio بيانات تعبئة الشكل باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**SetShapeFillData** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes=$diagram->getPages()->getPage(0)->getShapes();

$i = 0;

while ($i<sizeof($shapes->getCount())) {

$shape = $shapes->get($i);

if ($shape->getNameU() == "rectangle" && $shape->getID() == 1) {

$shape->getFill()->getFillBkgnd()->setValue($diagram->getPages()->getPage(0)->getShapes()->getShape(0)->getFill()->getFillBkgnd()->getValue());

$shape->getFill()->getFillForegnd()->setValue("#ebf8df");

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SetShapeFillData.vdx",$saveFileFormat->VDX);

print "Set visio shape's fill data.".PHP_EOL;

}

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**ضبط Visio بيانات تعبئة الشكل (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeFillData.php)
