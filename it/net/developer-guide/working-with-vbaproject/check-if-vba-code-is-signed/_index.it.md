---
title: Controlla se il codice VBA è firmato
type: docs
weight: 100
url: /it/net/check-if-vba-code-is-signed/
description: Controlla se il codice vba è firmato con la libreria Aspose.Diagram.
---
{{% alert color="primary" %}}

Aspose.Diagram consente all'utente di verificare se il progetto in codice VBA è firmato o meno. Si prega di utilizzare il[**Diagram.VbaProject.IsSigned**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbaproject/properties/issigned) proprietà per verificare se il progetto di codice VBA è firmato o meno.

{{% /alert %}}

 Il codice seguente spiega come verificare se il codice VBA è firmato o meno utilizzando il file[**Diagram.VbaProject.IsSigned**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbaproject/properties/issigned) proprietà. Puoi utilizzare uno qualsiasi dei tuoi file visio per testare questo codice. A scopo di test, è possibile utilizzare[questo file visio utilizzato nel codice](1.vsdm).

## Codice di esempio


{{< highlight csharp >}}

// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");

// Signature is valid
Console.WriteLine("Is VBA Code Project Signed: " + diagram.VbaProject.IsSigned);

diagram.Save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}


## Uscita console

 Di seguito è riportato l'output della console del codice precedente utilizzando il file[file di esempio visio](1out.vsdm) fornito dal link.

{{< highlight "java" >}}

Is VBA Code Project Signed: False

{{< /highlight >}}
