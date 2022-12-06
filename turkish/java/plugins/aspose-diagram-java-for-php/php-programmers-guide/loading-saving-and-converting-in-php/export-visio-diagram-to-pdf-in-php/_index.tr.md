---
title: Visio Diagram'i PHP'de PDF'ye aktar
type: docs
weight: 40
url: /tr/java/export-visio-diagram-to-pdf-in-php/
---
## **Aspose.Diagram - Visio Diagram'i PDF'ye aktar**
 Visio Diagram'i kullanarak PDF'ye Aktarmak için**PHP için Aspose.Diagram Java** , sadece çağırmak**ExportToPdf** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as PDF file format

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.pdf", $saveFileFormat->PDF);

print "Exported visio diagram to pdf.".PHP_EOL;

{{< /highlight >}}
## **Çalışan Kodu İndir**
İndirmek**Visio Diagram'i PDF'ye aktar (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToPdf.php)
