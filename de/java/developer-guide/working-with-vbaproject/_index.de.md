---
title: Verwalten Sie VBA-Codes von Visio Macro-Enabled diagram.
linktitle: Diagram VBA-Projekt
type: docs
weight: 200
url: /de/java/working-with-vbaproject/
description: VBA-Modul hinzufügen und VBA oder Makro mit Aspose.Diagram-Bibliothek ändern.
---
## **Fügen Sie ein VBA-Modul hinzu**
{{% alert color="primary" %}}

Aspose.Diagram ermöglicht Ihnen, ein neues VBA-Modul und Makrocode mit Aspose.Diagram hinzuzufügen. Bitte verwenden Sie die Methode [**Diagram.VbaProject.Modules.Add()**], um das neue VBA-Modul in diagram hinzuzufügen

{{% /alert %}}

 Der folgende Beispielcode fügt ein neues VBA-Modul und Makrocode hinzu und speichert die Ausgabe im Format VSDM. Einmal öffnen Sie die Ausgabedatei VSDM in Microsoft Visio und klicken auf die**Entwickler > Visual Basic** Menübefehle sehen Sie ein Modul namens "TestModule" und darin sehen Sie den folgenden Makrocode.

{{< highlight "java" >}}

 Sub ShowMessage()

    MsgBox "Welcome to Aspose!"

End Sub

{{< /highlight >}}

Hier ist der Beispielcode zum Generieren der Ausgabedatei VSDM mit VBA-Modul und Makrocode.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
//Add module
int index = diagram.getVbaProject().getModules().add(VbaModuleType.PROCEDURAL, "TestModule");
//Get module 
com.aspose.diagram.VbaModule module = diagram.getVbaProject().getModules().get(index);
//Set module
module.setCodes("Attribute VB_Name = \"module2\"\r\n Sub Button1_Click()\r\n\r\n    MsgBox \"Welcome to Aspose!\"\r\n\r\nEnd Sub\r\n");

diagram.save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

## **Ändern Sie VBA oder Makro**

{{% alert color="primary" %}} 

Sie können VBA- oder Makrocode mit Aspose.Diagram ändern. Aspose.Diagram hat den folgenden Namespace und die folgenden Klassen hinzugefügt, um das VBA-Projekt in der Datei Visio zu lesen und zu ändern.

- Aspose.Diagram.Vba
- VbaProjekt
- VbaModuleCollection
- VbaModul

Dieser Artikel zeigt Ihnen, wie Sie den VBA- oder Makrocode in der Quelldatei Visio mithilfe von Aspose.Diagram ändern.

{{% /alert %}} 

Der folgende Beispielcode lädt die Quelldatei Visio, die den folgenden VBA- oder Makrocode enthält

{{< highlight "java" >}}

 Sub Button1_Click()

    MsgBox "This is test message."

End Sub

{{< /highlight >}}

Nach der Ausführung des Beispielcodes Aspose.Diagram wird der VBA- oder Makrocode wie folgt geändert

{{< highlight "java" >}}

 Sub Button1_Click()

    MsgBox "This is Aspose.Diagram message."

End Sub

{{< /highlight >}}

 Sie können die herunterladen[Quelldatei Visio]() und die[Ausgabedatei Visio]() aus den angegebenen Links.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
//Get module 
com.aspose.diagram.VbaModule module = diagram.getVbaProject().getModules().get(2);
//Set module
module.setCodes("Attribute VB_Name = \"module2\"\r\n Sub Button1_Click()\r\n\r\n    MsgBox \"This is Aspose.Diagram message.\"\r\n\r\nEnd Sub\r\n");

diagram.save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

## **Themen vorantreiben**
- [Überprüfen Sie, ob der VBA-Code signiert ist](/diagram/de/java/check-if-vba-code-is-signed/)
