---
title: PHP'de Çizim Yazı Tipi Bilgilerini Alın
type: docs
weight: 40
url: /tr/java/retrieve-drawing-font-information-in-php/
---
## **Aspose.Diagram - Çizim Yazı Tipi Bilgilerini Al**
 Kullanarak Çizim Yazı Tipi Bilgilerini Almak İçin**PHP için Aspose.Diagram Java** , sadece çağırmak**GetDiagramFontInfo** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."drawing.vsd");

$fonts = $diagram->getFonts();

$i = 0;

while ($i<sizeof($fonts->getCount())) {

$font = $fonts->get($i);

\# Display information about the fonts

print $font->getName();

$i+=1;

}

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Çizim Yazı Tipi Bilgilerini Al (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/GetDiagramFontInfo.php)
