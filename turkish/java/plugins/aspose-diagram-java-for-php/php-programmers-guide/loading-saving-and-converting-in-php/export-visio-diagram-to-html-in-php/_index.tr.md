---
title: PHP'de Visio Diagram'i HTML'ye aktar
type: docs
weight: 20
url: /tr/java/export-visio-diagram-to-html-in-php/
---
## **Aspose.Diagram - Visio Diagram'i HTML'ye aktar**
 Visio Diagram'i kullanarak HTML'ye dışa aktarmak için**PHP için Aspose.Diagram Java** , sadece çağırmak**ExportToHtml** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as Html

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.html", $saveFileFormat->HTML);

print "Exported visio diagram to HTML.".PHP_EOL;

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Diagram'i HTML'ye aktar (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToHtml.php)
