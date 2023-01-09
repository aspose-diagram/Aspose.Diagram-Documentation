---
title: PHP'de Visio Diagram'i XAML'e dışa aktarın
type: docs
weight: 60
url: /tr/java/export-visio-diagram-to-xaml-in-php/
---
## **Aspose.Diagram - İhracat Visio Diagram ila XAML**
 Visio Diagram'i kullanarak XAML'e dışa aktarmak için**PHP için Aspose.Diagram Java** , sadece çağırmak**ExportToXaml** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."Drawing.vsd");

\# Save as XAML

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.xaml", $saveFileFormat->XAML);

print "Exported visio diagram to XAML.".PHP_EOL;

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Dışa aktarma Visio Diagram ila XAML (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXaml.php)
