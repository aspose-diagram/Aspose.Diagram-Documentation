---
title: قم بإنشاء خلية معرّفة من قبل المستخدم في ورقة الشكل بلغة PHP
type: docs
weight: 10
url: /ar/java/create-user-defined-cell-in-the-shapesheet-in-php/
---
## **Aspose.Diagram - تكوين خلية معرّفة من قبل المستخدم في ورقة الشكل**
 لإنشاء خلية معرّفة من قبل المستخدم في ورقة الشكل باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**CreateUserDefinedCell** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir . "Drawing.vsd");

$pages=$diagram->getPages();

$i=0;

while($i<(int)(string)$pages->getCount()) {

$page = $pages->get($i);

$shapes = $page->getShapes();

$j = 0;

while ($j<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($j);

if ($shape->getNameU() == "Process") {

\# Initialize user object

$user = new User();

$user->setName("UserDefineCell");

$user->getValue()->setVal("800");

\# Add user-defined cell

$shape->getUsers()->add($user);

}

$j += 1;

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir . "UserDefinedCells.vdx", $saveFileFormat->VDX);

print "Created User-defined Cell in the ShapeSheet.".PHP_EOL;

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**تكوين خلية معرّفة من قبل المستخدم في ورقة الشكل (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/CreateUserDefinedCell.php)
