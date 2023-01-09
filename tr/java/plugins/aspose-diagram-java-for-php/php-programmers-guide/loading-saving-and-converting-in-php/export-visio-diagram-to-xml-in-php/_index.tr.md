---
title: Visio Diagram'i PHP'de XML'e aktar
type: docs
weight: 70
url: /tr/java/export-visio-diagram-to-xml-in-php/
---
## **Aspose.Diagram - VSD'den VDX'e dışa aktarılıyor**
kullanarak VSD'i VDX'e dışa aktarmak için**PHP için Aspose.Diagram Java** , aramak**export_to_vdx** yöntemi**ExportToXml** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 public static function export_to_vdx($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.vdx", $saveFileFormat->VDX);

print "Exported visio diagram to VDX.".PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Diagram - VSD'den VSX'e dışa aktarılıyor**
kullanarak VSD'i VSX'e dışa aktarmak için**PHP için Aspose.Diagram Java** , aramak**export_to_vsx** yöntemi**ExportToXml** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 public static function export_to_vsx($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as VSX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.vsx", $saveFileFormat->VSX);

print "Exported visio diagram to VSX.".PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Diagram - VSD'den VTX'e dışa aktarılıyor**
kullanarak VSD'i VTX'e dışa aktarmak için**PHP için Aspose.Diagram Java** , aramak**export_to_vtx** yöntemi**ExportToXml** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 public static function export_to_vtx($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as VTX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.vtx", $saveFileFormat->VTX);

print "Exported visio diagram to VTX.".PHP_EOL;

}

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Diagram'i XML'e aktar (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXml.php)
