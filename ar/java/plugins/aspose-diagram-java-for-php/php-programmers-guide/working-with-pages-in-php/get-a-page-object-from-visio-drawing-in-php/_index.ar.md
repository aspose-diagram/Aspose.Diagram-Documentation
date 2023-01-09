---
title: احصل على كائن صفحة من Visio الرسم في PHP
type: docs
weight: 10
url: /ar/java/get-a-page-object-from-visio-drawing-in-php/
---
## **Aspose.Diagram - الحصول على كائن صفحة بواسطة المعرف**
 للحصول على كائن صفحة عن طريق المعرف باستخدام**Aspose.Diagram Java لـ PHP** ، مكالمة**get_page_object_by_id** طريقة**GetPageObject** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 public static function get_page_object_by_id($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

$page_id = 0;

\# Get page object by id

$page = $diagram->getPages()->getPage($page_id);

print "Page : ".(string)$page.PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Diagram - الحصول على كائن صفحة بالاسم**
 للحصول على كائن صفحة بالاسم باستخدام**Aspose.Diagram Java لـ PHP** ، مكالمة**get_page_object_by_name** طريقة**GetPageObject** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 public static function get_page_object_by_name($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Set page name

$page_name = "Flow 1";

\# Get page object by name

$page = $diagram->getPages()->getPage($page_name);

print "Page : ".(string)$page.PHP_EOL;

}

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**الحصول على كائن صفحة من رسم Visio (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/GetPageObject.php)
