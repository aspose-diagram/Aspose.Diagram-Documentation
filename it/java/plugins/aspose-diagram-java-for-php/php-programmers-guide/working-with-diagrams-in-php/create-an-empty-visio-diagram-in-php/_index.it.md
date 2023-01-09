---
title: Crea un Visio Diagram vuoto in PHP
type: docs
weight: 20
url: /it/java/create-an-empty-visio-diagram-in-php/
---
## **Aspose.Diagram - Crea un vuoto Visio Diagram**
 Per creare un vuoto Visio Diagram utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**Crea diagramma** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram();

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."CreateDiagram.vdx", $saveFileFormat->VDX);

print "Created visio diagram successfully!".PHP_EOL;

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Crea un vuoto Visio Diagram (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/CreateDiagram.php)
