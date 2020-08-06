---
title: Export Visio Diagram to XML in PHP
type: docs
weight: 70
url: /java/export-visio-diagram-to-xml-in-php/
---

## **Aspose.Diagram - Exporting VSD to VDX**
To Export VSD to VDX using **Aspose.Diagram Java for PHP**, call **export_to_vdx** method of **ExportToXml** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 public static function export_to_vdx($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.vdx", $saveFileFormat->VDX);

print "Exported visio diagram to VDX.".PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Diagram - Exporting VSD to VSX**
To Export VSD to VSX using **Aspose.Diagram Java for PHP**, call **export_to_vsx** method of **ExportToXml** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 public static function export_to_vsx($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as VSX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.vsx", $saveFileFormat->VSX);

print "Exported visio diagram to VSX.".PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Diagram - Exporting VSD to VTX**
To Export VSD to VTX using **Aspose.Diagram Java for PHP**, call **export_to_vtx** method of **ExportToXml** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 public static function export_to_vtx($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as VTX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.vtx", $saveFileFormat->VTX);

print "Exported visio diagram to VTX.".PHP_EOL;

}

{{< /highlight >}}
## **Download Running Code**
Download **Export Visio Diagram to XML (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXml.php)
- [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/LoadingSavingandConverting/ExportToXml.php)
