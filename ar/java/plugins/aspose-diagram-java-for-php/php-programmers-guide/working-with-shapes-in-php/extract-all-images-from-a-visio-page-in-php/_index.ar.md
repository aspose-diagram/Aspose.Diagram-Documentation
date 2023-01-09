---
title: استخراج كافة الصور من صفحة Visio بلغة PHP
type: docs
weight: 30
url: /ar/java/extract-all-images-from-a-visio-page-in-php/
---
## **Aspose.Diagram - استخراج كافة الصور من صفحة Visio**
 لاستخراج كافة الصور من صفحة Visio باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**استخراج الصور** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."drawing.vsd");

$shapes = $diagram->getPages()->getPage("Flow 1")->getShapes();

$i = 0;

$typeValue=new TypeValue();

while ($i <(int)(string)$shapes->getCount()){

$shape = $shapes->get($i);

\# Filter shapes by type Foreign

if ($shape->getType()== $typeValue->FOREIGN){

\# create an image file

$fos = new FileOutputStream($dataDir."Image#{i}.bmp");

$fos->write($shape->getForeignData()->getValue());

$fos->close();

}

$i += 1;

}

print "Extracted images successfully!".PHP_EOL;

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**استخراج كافة الصور من صفحة Visio (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ExtractImages.php)
