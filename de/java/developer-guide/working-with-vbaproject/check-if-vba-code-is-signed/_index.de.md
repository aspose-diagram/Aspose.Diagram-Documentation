---
title: Überprüfen Sie, ob der VBA-Code signiert ist
type: docs
weight: 100
url: /de/java/check-if-vba-code-is-signed/
description: Überprüfen Sie, ob der VBA-Code mit der Bibliothek Aspose.Diagram signiert ist.
---
{{% alert color="primary" %}}

Aspose.Diagram ermöglicht dem Benutzer zu überprüfen, ob das VBA-Codeprojekt signiert ist oder nicht. Bitte verwenden Sie die Eigenschaft [**Diagram.VbaProject.IsSigned**], um zu prüfen, ob das VBA-Codeprojekt signiert ist oder nicht.

{{% /alert %}}

 Der folgende Code erklärt, wie Sie mit der Eigenschaft [**Diagram.VbaProject.IsSigned**] überprüfen können, ob der VBA-Code signiert ist oder nicht. Sie können jede Ihrer visio-Dateien verwenden, um diesen Code zu testen. Zu Testzwecken können Sie verwenden[diese visio-Datei, die im Code verwendet wird](1.vsdm).

## Beispielcode


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


## Konsolenausgabe

 Unten ist die Konsolenausgabe des obigen Codes mit der[Beispieldatei visio](1out.vsdm) bereitgestellt durch den Link.

{{< highlight "java" >}}

Is VBA Code Project Signed: False

{{< /highlight >}}
