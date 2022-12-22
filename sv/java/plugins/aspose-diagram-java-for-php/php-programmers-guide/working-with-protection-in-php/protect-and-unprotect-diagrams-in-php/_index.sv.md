---
title: Skydda och avskydda diagram i PHP
type: docs
weight: 20
url: /sv/java/protect-and-unprotect-diagrams-in-php/
---
## **Aspose.Diagram - Skydda och ta bort skyddsdiagram**
 För att skydda och avskydda diagram med hjälp av**Aspose.Diagram Java för PHP** , helt enkelt åberopa**ProtectUnprotectDiagram** modul. Här kan du se exempelkod.

**PHP-kod**

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
## **Ladda ner Running Code**
 Ladda ner**Skydda och ta bort skyddsdiagram (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithProtection/ProtectUnprotectDiagram.php)
