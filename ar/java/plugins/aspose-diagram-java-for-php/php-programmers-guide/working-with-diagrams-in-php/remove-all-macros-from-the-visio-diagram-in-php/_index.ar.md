---
title: قم بإزالة كافة وحدات الماكرو من Visio Diagram في PHP
type: docs
weight: 30
url: /ar/java/remove-all-macros-from-the-visio-diagram-in-php/
---
## **Aspose.Diagram - إزالة كافة وحدات الماكرو من Visio Diagram**
 لإزالة كافة وحدات الماكرو من Visio Diagram باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**RemoveAllMacrosFromDiagram** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."drawing.vsd");

\# remove all macros

$diagram->setVbProjectData(null);

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."RemoveAllMacros.vdx", $saveFileFormat->VDX);

print "Removed all macros from diagram successfully!".PHP_EOL;

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**قم بإزالة كافة وحدات الماكرو من Visio Diagram (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/RemoveAllMacrosFromDiagram.php)
