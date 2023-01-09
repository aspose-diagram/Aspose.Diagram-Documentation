---
title: PHP'de Visio Diagram'i SVG'e dışa aktarın
type: docs
weight: 50
url: /tr/java/export-visio-diagram-to-svg-in-php/
---
## **Aspose.Diagram - İhracat Visio Diagram ila SVG**
 Visio Diagram'i kullanarak SVG'e dışa aktarmak için**PHP için Aspose.Diagram Java** , sadece çağırmak**ExportToSvg** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as SVG

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.svg", $saveFileFormat->SVG);

print "Exported visio diagram to SVG.".PHP_EOL;

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Dışa aktarma Visio Diagram ila SVG (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToSvg.php)
