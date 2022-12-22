---
title: تنزيل وتهيئة Aspose.Diagram في PHP
type: docs
weight: 10
url: /ar/java/download-and-configure-aspose-diagram-in-php/
---
## **تحميل المكتبات المطلوبة**
تحميل المكتبات المطلوبة المذكورة أدناه. هذه هي المطلوبة لتنفيذ Aspose.Diagram Java لأمثلة روبي.

- [Aspose.Diagram for Java مكون](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram)
## **تنزيل أمثلة من مواقع الترميز الاجتماعي**
الإصدارات التالية من الأمثلة قيد التشغيل متاحة للتنزيل على مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/tree/master/Plugins/Aspose_Diagram_Java_for_PHP)
## **التثبيت**
إنه بسيط للغاية وسهل التثبيت Aspose.Diagram Java لـ PHP ، يرجى اتباع التعليمات:

قم بتشغيل الأمر التالي.

{{< highlight "java" >}}

 $ gem install asposediagramjava

{{< /highlight >}}
## **استخدام**
قم بتضمين الملفات المطلوبة لتصدير رسم visio إلى وثيقة Pdf.

{{< highlight "java" >}}

 require File.dirname(File.dirname(File.dirname(__FILE__))) + '/lib/asposediagramjava'

include Asposediagramjava

include Asposediagramjava::ExportToPdf

initialize_aspose_Diagram

{{< /highlight >}}

دعونا نفهم الكود أعلاه.

1. يتأكد السطر الأول من تحميل Aspose.Diagram وإتاحته.
1. قم بتضمين الملفات المطلوبة للوصول إلى Aspose.Diagram
1. تهيئة المكتبات. يتم تحميل فئات aspose Java من المسار المتوفر في ملف aspose.yml
