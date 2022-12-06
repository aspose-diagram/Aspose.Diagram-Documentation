---
title: قم بتدوير شكل بزاوية مناسبة في PHP
type: docs
weight: 80
url: /ar/java/rotate-a-shape-with-suitable-angle-in-php/
---
## **Aspose.Diagram - قم بتدوير شكل بزاوية مناسبة**
 لتدوير شكل بزاوية مناسبة باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**استدارة** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."Drawing.vsd");

\# Add a shape and set the angle

$diagram->getPages()->getPage(0)->getShapes()->getShape(1)->setAngle(190);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."RotateShape.vdx",$saveFileFormat->VDX);

print "Rotated shape.".PHP_EOL;

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**تدوير شكل بزاوية مناسبة (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/RotateShape.php)
