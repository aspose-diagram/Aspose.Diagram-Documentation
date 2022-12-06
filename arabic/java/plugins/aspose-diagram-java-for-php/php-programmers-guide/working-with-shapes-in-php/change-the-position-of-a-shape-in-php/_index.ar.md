---
title: تغيير موضع الشكل في PHP
type: docs
weight: 10
url: /ar/java/change-the-position-of-a-shape-in-php/
---
## **Aspose.Diagram - تغيير موضع الشكل**
 لتغيير موضع الشكل باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**ChangeShapePosition** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes=$diagram->getPages()->getPage(0)->getShapes();

$i = 0;

while ($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

if ($shape->getNameU() == "Process" && (int)(string)$shape->getID() == 2) {

$shape->move(1, 1);

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."ChangeShapePosition.vdx",$saveFileFormat->VDX);

print"Changed postion of a shape.".PHP_EOL;

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**تغيير موضع الشكل (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ChangeShapePosition.php)
