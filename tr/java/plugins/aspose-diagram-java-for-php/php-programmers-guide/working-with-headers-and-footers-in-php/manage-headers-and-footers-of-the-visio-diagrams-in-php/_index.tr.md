---
title: PHP'de Visio Diyagramlarının Üstbilgilerini ve Altbilgilerini Yönetin
type: docs
weight: 10
url: /tr/java/manage-headers-and-footers-of-the-visio-diagrams-in-php/
---
## **Aspose.Diagram - Visio Diyagramlarının Üstbilgilerini ve Altbilgilerini Yönet**
 Kullanarak Visio Diyagramlarının Üstbilgilerini ve Altbilgilerini Yönetmek için**PHP için Aspose.Diagram Java** , sadece çağırmak**Üst Bilgiler ve Alt Bilgiler** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."drawing.vsd");

\# add page number at the right corner of header

$diagram->getHeaderFooter()->setHeaderRight("&p");

\# set text at the center

$diagram->getHeaderFooter()->setHeaderCenter("Center of the header");

\# set text at the left side

$diagram->getHeaderFooter()->setHeaderLeft("Left of the header");

\# add text at the right corner of footer

$diagram->getHeaderFooter()->setFooterRight("Right of the footer");

\# set text at the center

$diagram->getHeaderFooter()->setFooterCenter("Center of the footer");

\# set text at the left side

$diagram->getHeaderFooter()->setFooterLeft("Left of the footer");

\# set header & footer color

$color=new Color();

$diagram->getHeaderFooter()->setHeaderFooterColor($color->getRed());

\# set text font properties

$diagram->getHeaderFooter()->getHeaderFooterFont()->setItalic(1);

$diagram->getHeaderFooter()->getHeaderFooterFont()->setUnderline(0);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."HeadersAndFooters.vdx", $saveFileFormat->VDX);

print "Done with headers and footers.".PHP_EOL;

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Diyagramlarının Üst Bilgilerini ve Alt Bilgilerini Yönetin (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithHeadersandFooters/HeadersAndFooters.php)
