---
title: 在 PHP 中将 Visio Diagram 导出到 XML
type: docs
weight: 70
url: /zh/java/export-visio-diagram-to-xml-in-php/
---
## **Aspose.Diagram - 出口 VSD 到 VDX**
将 VSD 导出到 VDX 使用**Aspose.Diagram Java 用于 PHP**， 称呼**export_to_vdx**的方法**导出到Xml**模块。在这里您可以看到示例代码。

**PHP代码**

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
## **Aspose.Diagram - 出口 VSD 到 VSX**
将 VSD 导出到 VSX 使用**Aspose.Diagram Java 用于 PHP**， 称呼**export_to_vsx**的方法**导出到Xml**模块。在这里您可以看到示例代码。

**PHP代码**

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
## **Aspose.Diagram - 出口 VSD 到 VTX**
将 VSD 导出到 VTX 使用**Aspose.Diagram Java 用于 PHP**， 称呼**export_to_vtx**的方法**导出到Xml**模块。在这里您可以看到示例代码。

**PHP代码**

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
## **下载运行代码**
下载**将 Visio Diagram 导出到 XML (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXml.php)
