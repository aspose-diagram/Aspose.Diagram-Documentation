---
title: تصدير Visio Diagram إلى XPS في PHP
type: docs
weight: 80
url: /ar/java/export-visio-diagram-to-xps-in-php/
---
## **Aspose.Diagram - تصدير Visio Diagram إلى XPS**
 لتصدير Visio Diagram إلى XPS باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**ExportToXps** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as XPS

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.xps", $saveFileFormat->XPS);

print "Exported visio diagram to XPS.".PHP_EOL;

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**تصدير Visio Diagram إلى XPS (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXps.php)
