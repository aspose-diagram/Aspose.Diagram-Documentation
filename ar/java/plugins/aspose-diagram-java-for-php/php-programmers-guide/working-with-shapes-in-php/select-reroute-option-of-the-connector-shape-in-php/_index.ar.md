---
title: حدد خيار إعادة التوجيه لشكل الموصل في PHP
type: docs
weight: 90
url: /ar/java/select-reroute-option-of-the-connector-shape-in-php/
---
## **Aspose.Diagram - حدد خيار إعادة التوجيه لشكل الموصل**
 لتحديد خيار إعادة التوجيه لشكل الموصل باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**حدد خيار إعادة التوجيه** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."Drawing.vsd");

\# Access a particular page

$page=$diagram->getPages()->getPage("Flow 1");

\# get a particular connector shape

$shape=$page->getShapes()->getShape(1);

\# set reroute option

$conFixedCodeValue=new ConFixedCodeValue();

$shape->getLayout()->getConFixedCode()->setValue($conFixedCodeValue->NEVER_REROUTE);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SelectRerouteOption.vdx", $saveFileFormat->VDX);

print "Seleted reroute option of the connector shape.".PHP_EOL;

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**حدد خيار إعادة التوجيه لشكل الموصل (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SelectRerouteOption.php)
