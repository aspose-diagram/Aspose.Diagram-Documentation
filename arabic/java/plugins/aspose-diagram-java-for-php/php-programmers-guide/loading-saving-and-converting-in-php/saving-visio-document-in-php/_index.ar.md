---
title: حفظ Visio المستند في PHP
type: docs
weight: 100
url: /ar/java/saving-visio-document-in-php/
---
## **Aspose.Diagram - حفظ Visio وثيقة**
 لحفظ Visio المستند باستخدام**Aspose.Diagram Java لـ PHP**، يمكنك استخدام الكود التالي.

**كود PHP**

{{< highlight "php" >}}

 # Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram=new Diagram();

$diagram->save($dataDir."Diagram.vdx", $saveFileFormat->VDX);

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**تصدير Visio Diagram إلى XPS (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/SavingVisioDocument.php)
