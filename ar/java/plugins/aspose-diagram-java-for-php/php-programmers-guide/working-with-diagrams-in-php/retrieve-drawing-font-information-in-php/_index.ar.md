---
title: استرداد معلومات خط الرسم في PHP
type: docs
weight: 40
url: /ar/java/retrieve-drawing-font-information-in-php/
---
## **Aspose.Diagram - استرجاع معلومات خط الرسم**
 لاسترداد معلومات خط الرسم باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**GetDiagramFontInfo** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."drawing.vsd");

$fonts = $diagram->getFonts();

$i = 0;

while ($i<sizeof($fonts->getCount())) {

$font = $fonts->get($i);

\# Display information about the fonts

print $font->getName();

$i+=1;

}

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**استرداد معلومات خط الرسم (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/GetDiagramFontInfo.php)
