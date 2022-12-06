---
title: احصل على كائن رئيسي من الرسم في PHP
type: docs
weight: 20
url: /ar/java/get-master-object-from-drawing-in-php/
---
## **Aspose.Diagram - الحصول على كائن رئيسي بواسطة المعرف**
 للحصول على كائن رئيسي عن طريق المعرف باستخدام**Aspose.Diagram Java لـ PHP** ، مكالمة**get_master_object_by_id** طريقة**GetMasterObject** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 public static function get_master_object_by_id($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

$master_id = 2;

\# Get master object by id

$master = $diagram->getMasters()->getMaster($master_id);

print "Master ID : ".(string)$master->getID().PHP_EOL;

print "Master Name : ".(string)$master->getName().PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Diagram - الحصول على كائن رئيسي بالاسم**
 للحصول على كائن رئيسي بالاسم باستخدام**Aspose.Diagram Java لـ PHP** ، مكالمة**get_master_object_by_name** طريقة**GetMasterObject** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 public static function get_master_object_by_name($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Set master name

$master_name = "Background tranquil .2";

\# Get master object by name

$master = $diagram->getMasters()->getMasterByName($master_name);

print "Master ID : ".(string)$master->getID().PHP_EOL;

print "Master Name : ".(string)$master->getName().PHP_EOL;

}

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**الحصول على كائن رئيسي من الرسم (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/GetMasterObject.php)
