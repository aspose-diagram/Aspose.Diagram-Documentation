---
title: تصدير Visio Diagram إلى SVG في PHP
type: docs
weight: 50
url: /ar/java/export-visio-diagram-to-svg-in-php/
---
## **Aspose.Diagram - تصدير Visio Diagram إلى SVG**
 لتصدير Visio Diagram إلى SVG باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**ExportToSvg** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as SVG

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.svg", $saveFileFormat->SVG);

print "Exported visio diagram to SVG.".PHP_EOL;

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**تصدير Visio Diagram إلى SVG (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToSvg.php)
