---
title: Exporter Visio Diagram vers XML en PHP
type: docs
weight: 70
url: /fr/java/export-visio-diagram-to-xml-in-php/
---
## **Aspose.Diagram - Exportation VSD vers VDX**
Pour exporter VSD vers VDX en utilisant**Aspose.Diagram Java pour PHP** , appel**export_to_vdx** méthode de**Exporter versXml** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

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
## **Aspose.Diagram - Exportation VSD vers VSX**
Pour exporter VSD vers VSX en utilisant**Aspose.Diagram Java pour PHP** , appel**export_to_vsx** méthode de**Exporter versXml** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

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
## **Aspose.Diagram - Exportation VSD vers VTX**
Pour exporter VSD vers VTX en utilisant**Aspose.Diagram Java pour PHP** , appel**export_to_vtx** méthode de**Exporter versXml** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

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
## **Télécharger le code d'exécution**
 Télécharger**Exporter Visio Diagram vers XML (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXml.php)
