---
title: PHP'de Visio Diagram'in Izgaralarını, Cetvellerini, Kılavuzlarını ve Sayfa Sonlarını Gösterme ve Gizleme
type: docs
weight: 40
url: /tr/java/show-and-hide-grids-rulers-guides-and-page-breaks-of-the-visio-diagram-in-php/
---
## **Aspose.Diagram - Visio Diagram'in Izgaralarını, Cetvellerini, Kılavuzlarını ve Sayfa Sonlarını Göster ve Gizle**
Visio Diagram'in Izgaralarını, Cetvellerini, Kılavuzlarını ve Sayfa Sonlarını Göstermek ve Gizlemek İçin**PHP için Aspose.Diagram Java** , sadece çağırmak**ShowHideProperties** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram =new Diagram($dataDir."Drawing.vsd");

\# get window object by index

$window=$diagram->getWindows()->get(0);

\# set visibility of grid

$window->setShowGrid(1);

\# set visibility of guides

$window->setShowGuides(1);

\# set visibility of rulers

$window->setShowRulers(1);

\# set visibility of page breaks

$window->setShowPageBreaks(1);

\# save in any supported format

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."ShowHideProperties.vdx", $saveFileFormat->VDX);

print "Show and Hide Grids, Rulers, Guides and Page Breaks of the Visio Diagram.".PHP_EOL;

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Diagram'in (Aspose.Diagram) Izgaralarını, Cetvellerini, Kılavuzlarını ve Sayfa Sonlarını Gösterme ve Gizleme**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/ShowHideProperties.php)
