---
title: اقرأ الخلايا المعرفة من قبل المستخدم في PHP
type: docs
weight: 20
url: /ar/java/read-shape-s-user-defined-cells-in-php/
---
## **Aspose.Diagram - اقرأ الخلايا المعرفة بواسطة المستخدم للشكل**
 لقراءة الخلايا المحددة بواسطة المستخدم الخاصة بالشكل باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**ReadUserDefinedCells** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "drawing.vdx");

$shapes = $diagram->getPages()->getPage("Flow 1")->getShapes();

$i = 0;

while($i<(int)(string)$shapes->getCount()) {

$shape=$shapes->get($i);

if($shape->getNameU()=="Process") {

$users = $shape->getUsers();

$j = 0;

while ($j<(int)(string)$users->getCount()) {

$user = $users->get($j);

print $user->getName() . ": " . $user->getValue()->getVal();

$j += 1;

}

break;

}

$i+=1;

}

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**قراءة الخلايا المحددة بواسطة المستخدم الخاصة بالشكل (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/ReadUserDefinedCells.php)
