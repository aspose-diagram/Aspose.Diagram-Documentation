---
title: تصدير Visio Diagram إلى HTML في PHP
type: docs
weight: 20
url: /ar/java/export-visio-diagram-to-html-in-php/
---
## **Aspose.Diagram - تصدير Visio Diagram إلى HTML**
 لتصدير Visio Diagram إلى HTML باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**ExportToHtml** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as Html

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.html", $saveFileFormat->HTML);

print "Exported visio diagram to HTML.".PHP_EOL;

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**تصدير Visio Diagram إلى HTML (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToHtml.php)
