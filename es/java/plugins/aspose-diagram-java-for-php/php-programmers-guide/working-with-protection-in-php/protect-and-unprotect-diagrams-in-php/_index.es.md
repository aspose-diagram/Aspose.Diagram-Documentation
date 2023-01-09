---
title: Proteger y desproteger diagramas en PHP
type: docs
weight: 20
url: /es/java/protect-and-unprotect-diagrams-in-php/
---
## **Aspose.Diagram - Diagramas de protección y desprotección**
 Para proteger y desproteger diagramas usando**Aspose.Diagram Java para PHP** , simplemente invocar**ProtegerDesprotegerDiagrama** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

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
## **Descargar código de ejecución**
 Descargar**Diagramas de protección y desprotección (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithProtection/ProtectUnprotectDiagram.php)
