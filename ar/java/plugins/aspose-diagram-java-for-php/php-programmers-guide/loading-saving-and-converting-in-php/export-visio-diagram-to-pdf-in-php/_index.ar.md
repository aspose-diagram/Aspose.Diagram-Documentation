---
title: تصدير Visio Diagram إلى PDF في PHP
type: docs
weight: 40
url: /ar/java/export-visio-diagram-to-pdf-in-php/
---
## **Aspose.Diagram - تصدير Visio Diagram إلى PDF**
 لتصدير Visio Diagram إلى PDF باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**ExportToPdf** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as PDF file format

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.pdf", $saveFileFormat->PDF);

print "Exported visio diagram to pdf.".PHP_EOL;

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
تحميل**تصدير Visio Diagram إلى PDF (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToPdf.php)
