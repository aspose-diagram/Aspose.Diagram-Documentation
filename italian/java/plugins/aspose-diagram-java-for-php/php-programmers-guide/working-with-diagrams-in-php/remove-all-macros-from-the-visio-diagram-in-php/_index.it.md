---
title: Rimuovi tutte le macro da Visio Diagram in PHP
type: docs
weight: 30
url: /it/java/remove-all-macros-from-the-visio-diagram-in-php/
---
## **Aspose.Diagram - Rimuovi tutte le macro dal Visio Diagram**
 Per rimuovere tutte le macro dal Visio Diagram utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**Rimuovi tutte le macro dal diagramma** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

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
## **Scarica il codice in esecuzione**
 Scarica**Rimuovi tutte le macro da Visio Diagram (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/RemoveAllMacrosFromDiagram.php)
