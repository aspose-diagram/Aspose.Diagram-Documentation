---
title: تصدير Visio Diagram إلى XML في PHP
type: docs
weight: 70
url: /ar/java/export-visio-diagram-to-xml-in-php/
---
## **Aspose.Diagram - تصدير VSD الى VDX**
لتصدير VSD إلى VDX باستخدام**Aspose.Diagram Java لـ PHP** ، مكالمة**export_to_vdx** طريقة**ExportToXml** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

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
## **Aspose.Diagram - تصدير VSD الى VSX**
لتصدير VSD إلى VSX باستخدام**Aspose.Diagram Java لـ PHP** ، مكالمة**export_to_vsx** طريقة**ExportToXml** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

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
## **Aspose.Diagram - تصدير VSD الى VTX**
لتصدير VSD إلى VTX باستخدام**Aspose.Diagram Java لـ PHP** ، مكالمة**export_to_vtx** طريقة**ExportToXml** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

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
## **قم بتنزيل كود التشغيل**
 تحميل**تصدير Visio Diagram إلى XML (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXml.php)
