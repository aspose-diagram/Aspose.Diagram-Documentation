---
title: Überprüfen Sie, ob der VBA-Code signiert ist
type: docs
weight: 100
url: /de/net/check-if-vba-code-is-signed/
description: Überprüfen Sie, ob der VBA-Code mit der Bibliothek Aspose.Diagram signiert ist.
---
{{% alert color="primary" %}}

Aspose.Diagram ermöglicht dem Benutzer zu überprüfen, ob das VBA-Codeprojekt signiert ist oder nicht. Bitte verwenden Sie die[**Diagram.VbaProject.IsSigned**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbaproject/properties/issigned) -Eigenschaft, um zu überprüfen, ob das VBA-Codeprojekt signiert ist oder nicht.

{{% /alert %}}

 Der folgende Code erklärt, wie Sie überprüfen können, ob der VBA-Code signiert ist oder nicht, indem Sie die[**Diagram.VbaProject.IsSigned**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbaproject/properties/issigned) Eigentum. Sie können jede Ihrer visio-Dateien verwenden, um diesen Code zu testen. Zu Testzwecken können Sie verwenden[diese visio-Datei, die im Code verwendet wird](1.vsdm).

## Beispielcode

```
{{< highlight "csharp" >}}

// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");

// Signature is valid
Console.WriteLine("Is VBA Code Project Signed: " + diagram.VbaProject.IsSigned);

diagram.Save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

## Konsolenausgabe

 Unten ist die Konsolenausgabe des obigen Codes mit der[Beispieldatei visio](1out.vsdm) bereitgestellt durch den Link.

{{< highlight "java" >}}

Is VBA Code Project Signed: False

{{< /highlight >}}
