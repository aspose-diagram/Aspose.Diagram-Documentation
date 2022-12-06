---
title: PHP'deki Visio Diagram'den Tüm Makroları Kaldır
type: docs
weight: 30
url: /tr/java/remove-all-macros-from-the-visio-diagram-in-php/
---
## **Aspose.Diagram - Visio Diagram'den Tüm Makroları Kaldır**
 Visio Diagram'den Tüm Makroları Kaldırmak için**PHP için Aspose.Diagram Java** , sadece çağırmak**DiyagramdanTüm Makroları Kaldır** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."drawing.vsd");

\# remove all macros

$diagram->setVbProjectData(null);

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."RemoveAllMacros.vdx", $saveFileFormat->VDX);

print "Removed all macros from diagram successfully!".PHP_EOL;

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Diagram'den (Aspose.Diagram) Tüm Makroları Kaldır**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/RemoveAllMacrosFromDiagram.php)
