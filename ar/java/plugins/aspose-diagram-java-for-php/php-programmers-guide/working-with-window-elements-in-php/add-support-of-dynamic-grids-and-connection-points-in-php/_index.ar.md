---
title: أضف دعمًا للشبكات الديناميكية ونقاط الاتصال في PHP
type: docs
weight: 10
url: /ar/java/add-support-of-dynamic-grids-and-connection-points-in-php/
---
## **Aspose.Diagram - إضافة دعم للشبكات الديناميكية ونقاط الاتصال**
 لإضافة دعم للشبكات الديناميكية ونقاط الاتصال باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**AddDynamicGridsAndConnectionPoints** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

\# get window object by index

$window=$diagram->getWindows()->get(0);

\# check dynamic grid option

$window->setDynamicGridEnabled(1);

\# check connection points option

$window->setShowConnectionPoints(1);

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."AddDynamicGridsAndConnectionPoints.vsx", $saveFileFormat->VSX);

print "Added Support of Dynamic Grids and Connection Points in the Visio Drawings.".PHP_EOL;

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**إضافة دعم للشبكات الديناميكية ونقاط الاتصال (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/AddDynamicGridsAndConnectionPoints.php)
