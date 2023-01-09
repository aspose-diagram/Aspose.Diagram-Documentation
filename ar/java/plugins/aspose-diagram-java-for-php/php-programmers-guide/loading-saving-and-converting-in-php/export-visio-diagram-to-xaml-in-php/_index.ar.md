---
title: تصدير Visio Diagram إلى XAML في PHP
type: docs
weight: 60
url: /ar/java/export-visio-diagram-to-xaml-in-php/
---
## **Aspose.Diagram - تصدير Visio Diagram إلى XAML**
 لتصدير Visio Diagram إلى XAML باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**ExportToXaml** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."Drawing.vsd");

\# Save as XAML

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.xaml", $saveFileFormat->XAML);

print "Exported visio diagram to XAML.".PHP_EOL;

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**تصدير Visio Diagram إلى XAML (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXaml.php)
