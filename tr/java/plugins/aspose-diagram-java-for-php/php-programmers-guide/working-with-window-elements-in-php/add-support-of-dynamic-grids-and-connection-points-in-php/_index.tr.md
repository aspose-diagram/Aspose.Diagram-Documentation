---
title: PHP'de Dinamik Izgaralar ve Bağlantı Noktaları Desteği Ekleyin
type: docs
weight: 10
url: /tr/java/add-support-of-dynamic-grids-and-connection-points-in-php/
---
## **Aspose.Diagram - Dinamik Şebekeler ve Bağlantı Noktaları Desteği Ekleyin**
 Kullanarak Dinamik Izgaralar ve Bağlantı Noktaları Desteği Eklemek İçin**PHP için Aspose.Diagram Java** , sadece çağırmak**DynamicGridsAndConnectionPoints Ekle** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

\# get window object by index

$window=$diagram->getWindows()->get(0);

\# check dynamic grid option

$window->setDynamicGridEnabled(1);

\# check connection points option

$window->setShowConnectionPoints(1);

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."AddDynamicGridsAndConnectionPoints.vsx", $saveFileFormat->VSX);

print "Added Support of Dynamic Grids and Connection Points in the Visio Drawings.".PHP_EOL;

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Dinamik Şebekeler ve Bağlantı Noktaları Desteği Ekleyin (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/AddDynamicGridsAndConnectionPoints.php)
