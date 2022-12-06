---
title: PHP'de Şeklin Kullanıcı Tanımlı Hücrelerini Okuyun
type: docs
weight: 20
url: /tr/java/read-shape-s-user-defined-cells-in-php/
---
## **Aspose.Diagram - Şeklin Kullanıcı Tanımlı Hücrelerini Oku**
 Kullanarak Şeklin Kullanıcı Tanımlı Hücrelerini Okumak için**PHP için Aspose.Diagram Java** , sadece çağırmak**ReadUserDefinedCells** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

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
## **Çalışan Kodu İndir**
 İndirmek**Şeklin Kullanıcı Tanımlı Hücrelerini Oku (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/ReadUserDefinedCells.php)
