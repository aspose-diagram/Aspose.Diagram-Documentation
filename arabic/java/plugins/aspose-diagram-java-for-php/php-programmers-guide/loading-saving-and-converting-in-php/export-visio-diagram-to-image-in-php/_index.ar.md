---
title: تصدير Visio Diagram إلى Image في PHP
type: docs
weight: 30
url: /ar/java/export-visio-diagram-to-image-in-php/
---
## **Aspose.Diagram - تصدير Visio Diagram إلى صورة**
 لتصدير Visio Diagram إلى صورة باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**ExportToImage** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as PNG

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.png", $saveFileFormat->PNG);

print "Exported visio diagram to PNG.".PHP_EOL;

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**تصدير Visio Diagram إلى صورة (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToImage.php)
