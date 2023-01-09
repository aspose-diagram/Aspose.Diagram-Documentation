---
title: Visio Diagram'i PHP'de Görüntüye Aktar
type: docs
weight: 30
url: /tr/java/export-visio-diagram-to-image-in-php/
---
## **Aspose.Diagram - Visio Diagram'i Resme Aktar**
 Visio Diagram'i kullanarak Görüntüye Dışa Aktarmak için**PHP için Aspose.Diagram Java** , sadece çağırmak**Görüntüye Dışa Aktar** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as PNG

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.png", $saveFileFormat->PNG);

print "Exported visio diagram to PNG.".PHP_EOL;

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Diagram'i Resme Aktar (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToImage.php)
