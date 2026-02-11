---
title: Controlla se il codice VBA è firmato
type: docs
weight: 100
url: /it/java/check-if-vba-code-is-signed/
description: Controlla se il codice vba è firmato con la libreria Aspose.Diagram.
---
{{% alert color="primary" %}}

Aspose.Diagram consente all'utente di verificare se il progetto in codice VBA è firmato o meno. Utilizzare la proprietà [**Diagram.VbaProject.IsSigned**] per verificare se il progetto di codice VBA è firmato o meno.

{{% /alert %}}

 Il codice seguente spiega come verificare se il codice VBA è firmato o meno utilizzando la proprietà [**Diagram.VbaProject.IsSigned**]. Puoi utilizzare uno qualsiasi dei tuoi file visio per testare questo codice. A scopo di test, è possibile utilizzare[questo file visio utilizzato nel codice](1.vsdm).

## Codice di esempio


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
  
//Check signed     
boolean isSigned = diagram.getVbaProject().isSigned();

diagram.save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}


## Uscita console

 Di seguito è riportato l'output della console del codice precedente utilizzando il file[file di esempio visio](1out.vsdm) fornito dal link.

{{< highlight "java" >}}

Is VBA Code Project Signed: False

{{< /highlight >}}
