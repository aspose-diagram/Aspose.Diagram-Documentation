---
title: PHP'de ShapeSheet'te Kullanıcı Tanımlı Hücre Oluşturma
type: docs
weight: 10
url: /tr/java/create-user-defined-cell-in-the-shapesheet-in-php/
---
## **Aspose.Diagram - ShapeSheet'te Kullanıcı Tanımlı Hücre Oluştur**
 Kullanarak ShapeSheet'te Kullanıcı Tanımlı Hücre Oluşturmak İçin**PHP için Aspose.Diagram Java** , sadece çağırmak**Kullanıcı Tanımlı Hücre Oluştur** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

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
## **Çalışan Kodu İndir**
 İndirmek**ShapeSheet'te Kullanıcı Tanımlı Hücre Oluşturun (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/CreateUserDefinedCell.php)
