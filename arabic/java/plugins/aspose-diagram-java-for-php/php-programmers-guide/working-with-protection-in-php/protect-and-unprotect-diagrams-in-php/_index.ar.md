---
title: حماية الرسوم البيانية وإلغاء حمايتها في PHP
type: docs
weight: 20
url: /ar/java/protect-and-unprotect-diagrams-in-php/
---
## **Aspose.Diagram - حماية المخططات وإلغاء حمايتها**
 لحماية الرسوم التخطيطية وإلغاء حمايتها باستخدام**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**ProtectUnprotectDiagram** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "drawing.vsd");

$diagram->getDocumentSettings()->setProtectBkgnds(1);

$diagram->getDocumentSettings()->setProtectMasters(1);

$diagram->getDocumentSettings()->setProtectShapes(1);

$diagram->getDocumentSettings()->setProtectStyles(1);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir . "ProtectUnprotectDiagram.vdx", $saveFileFormat->VDX);

print "Applied protection on diagram successfully!".PHP_EOL;

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**حماية الرسوم التخطيطية وإلغاء حمايتها (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithProtection/ProtectUnprotectDiagram.php)
