---
title: اضبط مظهر شكل نوع الموصل في Visio في PHP
type: docs
weight: 100
url: /ar/java/set-appearance-of-the-connector-type-shape-in-visio-in-php/
---
## **Aspose.Diagram - ضبط مظهر شكل نوع الموصل في Visio**
 لتعيين مظهر شكل نوع الموصل في Visio باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**SetShapeAppearance** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram =new Diagram($dataDir."Drawing.vsd");

\# Access a particular page

$page=$diagram->getPages()->getPage("Flow 1");

\# get a particular connector shape

$shape=$page->getShapes()->getShape(1);

\# set dynamic connector appearance

$connectorsTypeValue=new ConnectorsTypeValue();

$shape->setConnectorsType($connectorsTypeValue->STRAIGHT_LINES);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SetShapeAppearance.vdx",$saveFileFormat->VDX);

print "Set appearnce of the connector type shape.".PHP_EOL;

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**اضبط مظهر شكل نوع الموصل في Visio (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeAppearance.php)
