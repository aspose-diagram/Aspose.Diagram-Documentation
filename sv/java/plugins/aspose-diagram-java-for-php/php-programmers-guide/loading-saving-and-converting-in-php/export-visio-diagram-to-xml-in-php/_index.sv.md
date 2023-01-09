---
title: Exportera Visio Diagram till XML i PHP
type: docs
weight: 70
url: /sv/java/export-visio-diagram-to-xml-in-php/
---
## **Aspose.Diagram - Exporterar VSD till VDX**
För att exportera VSD till VDX med hjälp av**Aspose.Diagram Java för PHP** , ringa upp**export_to_vdx** metod av**ExportToXml** modul. Här kan du se exempelkod.

**PHP-kod**

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
## **Aspose.Diagram - Exporterar VSD till VSX**
För att exportera VSD till VSX med hjälp av**Aspose.Diagram Java för PHP** , ringa upp**export_to_vsx** metod av**ExportToXml** modul. Här kan du se exempelkod.

**PHP-kod**

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
## **Aspose.Diagram - Exporterar VSD till VTX**
För att exportera VSD till VTX med hjälp av**Aspose.Diagram Java för PHP** , ringa upp**export_to_vtx** metod av**ExportToXml** modul. Här kan du se exempelkod.

**PHP-kod**

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
## **Ladda ner Running Code**
 Ladda ner**Exportera Visio Diagram till XML (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXml.php)
