---
title: PHP'de Bağlayıcı Şeklinin Yeniden Yönlendirme Seçeneğini Seçin
type: docs
weight: 90
url: /tr/java/select-reroute-option-of-the-connector-shape-in-php/
---
## **Aspose.Diagram - Bağlayıcı Şeklinin Yeniden Yönlendirme Seçeneğini Belirleyin**
 Kullanarak Bağlayıcı Şeklinin Yeniden Yönlendirme Seçeneğini Belirlemek İçin**Yakut için Aspose.Diagram Java** , sadece çağırmak**Yeniden Yönlendirme Seçeneği Seçin** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."Drawing.vsd");

\# Access a particular page

$page=$diagram->getPages()->getPage("Flow 1");

\# get a particular connector shape

$shape=$page->getShapes()->getShape(1);

\# set reroute option

$conFixedCodeValue=new ConFixedCodeValue();

$shape->getLayout()->getConFixedCode()->setValue($conFixedCodeValue->NEVER_REROUTE);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SelectRerouteOption.vdx", $saveFileFormat->VDX);

print "Seleted reroute option of the connector shape.".PHP_EOL;

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Konnektör Şeklinin Yeniden Yönlendirme Seçeneğini Belirleyin (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SelectRerouteOption.php)
