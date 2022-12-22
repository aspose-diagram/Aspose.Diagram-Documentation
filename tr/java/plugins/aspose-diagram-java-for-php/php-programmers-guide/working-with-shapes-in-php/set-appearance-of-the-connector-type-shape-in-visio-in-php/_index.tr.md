---
title: PHP'de Visio'de Bağlayıcı Türü Şeklinin Görünümünü Ayarlayın
type: docs
weight: 100
url: /tr/java/set-appearance-of-the-connector-type-shape-in-visio-in-php/
---
## **Aspose.Diagram - Visio'de Konektör Tipi Şeklin Görünümünü Ayarla**
 Visio'de Konektör Türü Şeklinin Görünümünü Ayarlamak İçin**PHP için Aspose.Diagram Java** , sadece çağırmak**SetShapeAppearance** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram =new Diagram($dataDir."Drawing.vsd");

\# Access a particular page

$page=$diagram->getPages()->getPage("Flow 1");

\# get a particular connector shape

$shape=$page->getShapes()->getShape(1);

\# set dynamic connector appearance

$connectorsTypeValue=new ConnectorsTypeValue();

$shape->setConnectorsType($connectorsTypeValue->STRAIGHT_LINES);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SetShapeAppearance.vdx",$saveFileFormat->VDX);

print "Set appearnce of the connector type shape.".PHP_EOL;

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio'de (Aspose.Diagram) Konektör Tipi Şeklin Görünümünü Ayarla**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeAppearance.php)
