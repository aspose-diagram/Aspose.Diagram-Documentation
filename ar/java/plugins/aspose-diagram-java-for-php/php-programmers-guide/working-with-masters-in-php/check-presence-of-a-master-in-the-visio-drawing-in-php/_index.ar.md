---
title: تحقق من وجود ماجستير في رسم Visio بلغة PHP
type: docs
weight: 10
url: /ar/java/check-presence-of-a-master-in-the-visio-drawing-in-php/
---
## **Aspose.Diagram - التحقق من وجود رئيسي بواسطة المعرف**
 للتحقق من وجود رئيسي عن طريق المعرف باستخدام**Aspose.Diagram Java لـ PHP** ، مكالمة**check_presence_master_by_id** طريقة**CheckPresenceOfMaster** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 public static function check_presence_master_by_id($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

$master_id = 2;

\# check master by id

$is_present = $diagram->getMasters()->isExist($master_id);

print "Master Presence : ".(string)$is_present.PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Diagram - التحقق من وجود رئيسي بالاسم**
 للتحقق من وجود رئيسي بالاسم باستخدام**Aspose.Diagram Java لـ PHP** ، مكالمة**check_presence_master_by_name** طريقة**CheckPresenceOfMaster** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 public static function check_presence_master_by_name($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."Drawing.vsd");

\# Set master name

$master_name = "Background tranquil .2";

\# check master object by name

$is_present = $diagram->getMasters()->isExist($master_name);

print "Master Presence : ".(string)$is_present.PHP_EOL;

}

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**تحقق من وجود ماجستير في رسم Visio (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/CheckPresenceOfMaster.php)
