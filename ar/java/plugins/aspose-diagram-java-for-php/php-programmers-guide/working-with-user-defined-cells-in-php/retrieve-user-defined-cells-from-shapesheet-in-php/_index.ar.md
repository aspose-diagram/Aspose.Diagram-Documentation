---
title: استرجع الخلايا المعرفة من قبل المستخدم من ورقة الأشكال في PHP
type: docs
weight: 30
url: /ar/java/retrieve-user-defined-cells-from-shapesheet-in-php/
---
## **Aspose.Diagram - استرداد الخلايا المعرفة من قبل المستخدم من ورقة الأشكال**
 لاسترداد الخلايا المعرفة من قبل المستخدم من الأشكال باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**GetUserDefinedCells** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir . "drawing.vdx");

$pages=$diagram->getPages();

$count=0;

while($count<(int)(string)$pages->getCount()) {

$page = $pages->get($count);

$shapes = $page->getShapes();

$i = 0;

while ($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

if ($shape->getNameU() == "Process") {

$users = $shape->getUsers();

$j = 0;

while ($j<(int)(string)$users->getCount()) {

$user = $users->get($j);

print "Name: " . $user->getNameU() . " Value: " . $user->getValue()->getVal() . " Prompt: " . $user->getPrompt()->getValue();

$j += 1;

}

break;

}

$i += 1;

}

$count += 1;

}

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**استرجاع الخلايا المعرفة من قبل المستخدم من ورقة الأشكال (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/GetUserDefinedCells.php)
