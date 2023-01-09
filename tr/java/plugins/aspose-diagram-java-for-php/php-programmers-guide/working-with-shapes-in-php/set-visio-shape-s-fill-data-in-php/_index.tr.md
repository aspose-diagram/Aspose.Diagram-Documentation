---
title: PHP'de Visio Shape's Fill verilerini ayarla
type: docs
weight: 130
url: /tr/java/set-visio-shape-s-fill-data-in-php/
---
## **Aspose.Diagram - Visio Shape's Fill verilerini ayarla**
 Visio Shape's Fill verilerini kullanarak ayarlamak için**Yakut için Aspose.Diagram Java** , sadece çağırmak**SetShapeFillData** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes=$diagram->getPages()->getPage(0)->getShapes();

$i = 0;

while ($i<sizeof($shapes->getCount())) {

$shape = $shapes->get($i);

if ($shape->getNameU() == "rectangle" && $shape->getID() == 1) {

$shape->getFill()->getFillBkgnd()->setValue($diagram->getPages()->getPage(0)->getShapes()->getShape(0)->getFill()->getFillBkgnd()->getValue());

$shape->getFill()->getFillForegnd()->setValue("#ebf8df");

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SetShapeFillData.vdx",$saveFileFormat->VDX);

print "Set visio shape's fill data.".PHP_EOL;

}

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Shape's Fill verilerini ayarla (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeFillData.php)
