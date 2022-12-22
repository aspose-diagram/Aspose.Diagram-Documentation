---
title: Exportar Visio Diagram a XML en PHP
type: docs
weight: 70
url: /es/java/export-visio-diagram-to-xml-in-php/
---
## **Aspose.Diagram - Exportando VSD a VDX**
Para exportar VSD a VDX usando**Aspose.Diagram Java para PHP** , llamar**exportar_a_vdx** método de**Exportar a Xml** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

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
## **Aspose.Diagram - Exportando VSD a VSX**
Para exportar VSD a VSX usando**Aspose.Diagram Java para PHP** , llamar**exportar_a_vsx** método de**Exportar a Xml** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

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
## **Aspose.Diagram - Exportando VSD a VTX**
Para exportar VSD a VTX usando**Aspose.Diagram Java para PHP** , llamar**exportar_a_vtx** método de**Exportar a Xml** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

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
## **Descargar código de ejecución**
 Descargar**Exportar Visio Diagram a XML (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXml.php)
