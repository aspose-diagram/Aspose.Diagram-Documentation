---
title: PHP'de Visio Diagram'i XPS'e dışa aktarın
type: docs
weight: 80
url: /tr/java/export-visio-diagram-to-xps-in-php/
---
## **Aspose.Diagram - İhracat Visio Diagram ila XPS**
 Visio Diagram'i kullanarak XPS'e dışa aktarmak için**PHP için Aspose.Diagram Java** , sadece çağırmak**ExportToXps** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as XPS

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.xps", $saveFileFormat->XPS);

print "Exported visio diagram to XPS.".PHP_EOL;

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Dışa aktarma Visio Diagram ila XPS (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXps.php)
