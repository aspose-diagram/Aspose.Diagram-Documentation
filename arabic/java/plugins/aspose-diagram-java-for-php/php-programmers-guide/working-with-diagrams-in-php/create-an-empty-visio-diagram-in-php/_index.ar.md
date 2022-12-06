---
title: قم بإنشاء Visio Diagram فارغًا في PHP
type: docs
weight: 20
url: /ar/java/create-an-empty-visio-diagram-in-php/
---
## **Aspose.Diagram - أنشئ Visio Diagram فارغًا**
 لإنشاء Visio Diagram فارغ باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**إنشاء رسم بياني** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram();

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."CreateDiagram.vdx", $saveFileFormat->VDX);

print "Created visio diagram successfully!".PHP_EOL;

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**إنشاء Visio Diagram (Aspose.Diagram) فارغ**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/CreateDiagram.php)
