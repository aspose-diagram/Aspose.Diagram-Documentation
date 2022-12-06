﻿---
title: Aspose.Diagram Font-Operationen
type: docs
weight: 180
url: /de/net/aspose-diagram-font-operations/
description: Auf dieser Seite wird beschrieben, wie Sie Schriftarten mit der Bibliothek Aspose.Diagram bearbeiten.
---
## **So geben Sie den Speicherort für TrueType-Schriftarten an**
Mit Aspose.Diagram können Entwickler die Schriftverzeichnisse zum Rendern in Visio-Diagrammen festlegen. Dieser Artikel zeigt, wie Sie Schriftarten aus benutzerdefinierten Verzeichnissen verwenden.
### **Arbeiten mit Schriftarten**
#### **Wobei Aspose.Diagram auf Windows nach TrueType-Schriftarten sucht**
 Aspose.Diagram sucht nach Schriften in der**Windows\Schriftarten** Mappe. Diese Standardeinstellung funktioniert die meiste Zeit, also geben Sie Ihre eigenen Schriftartenordner nur dann an, wenn Sie es wirklich brauchen.
#### **So geben Sie einen Schriftordner explizit an**
Aspose.Diagram APIs hat die FontDirs-Eigenschaft für die verfügbar gemacht[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) -Klasse, um die Schriftordner wie unten beschrieben anzugeben.

1. Die Eigenschaft Diagram.FontDirs akzeptiert ein String-Array, sodass Entwickler mit diesem Ansatz viele Schriftartverzeichnisse angeben können.

{{% alert color="primary" %}} 

Wenn Sie den Schriftartenordner mit dem oben genannten Ansatz angeben, empfehlen wir, den Speicherort der Schriftart am Anfang der Anwendung festzulegen, da Sie sonst möglicherweise schlecht formatierte Ergebnisse erhalten.

{{% /alert %}} {{% alert color="primary" %}} 

Das Festlegen des Schriftartenordners mit einer der oben genannten Methoden stellt nicht sicher, dass der Aspose.Diagram API nicht nach den Schriftarten an Standardspeicherorten wie dem Schriftartenordner des Systems sucht.

{{% /alert %}} 
#### **Programmierbeispiel**
Das folgende Codebeispiel zeigt, wie Sie Aspose.Diagram so einstellen, dass es beim Rendern oder Einbetten von Schriftarten in mehreren Ordnern nach TrueType-Schriftarten sucht.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-OS-Fonts-Location-SpecifyFontLocation-SpecifyFontLocation.cs" >}}
### **Erhalten Sie während des Renderns eine Benachrichtigung über fehlende Schriften und Schriftersetzungen**
Aspose.Diagram API benötigt Zugriff auf die genaue Schriftart, um die Zeichnung richtig in das PDF-Format zu rendern. Wenn die erforderliche Schriftart auf dem Computer nicht verfügbar ist, rendert Aspose.Diagram API jede Instanz dieser Schriftart mit der Standardschriftart oder der ähnlichsten verfügbaren Schriftart auf dem Computer, da diese Ersetzung das Aussehen der gerenderten Zeichnung ändern kann, müssen Entwickler möglicherweise sein benachrichtigt, wenn eine Schriftart fehlt und durch welche Schriftart sie ersetzt wird.
#### **Programmierbeispiel für Benachrichtigung über fehlende Schriftarten und Schriftartersetzung**
Um während des Renderns über die Ersetzung von Schriftarten benachrichtigt zu werden:

1. Erstellen Sie eine Klasse, die die implementiert[IWarnungRückruf](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback)
1. Übergeben Sie es an die PdfSaveOptions.WarningCallback-Eigenschaft.

Beim Speichern der Zeichnung wird die Instanz von[IWarnungRückruf](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback)wird aufgerufen, wenn es potenzielle Genauigkeitsprobleme mit der Zeichnung gibt. In diesem Fall entscheiden wir uns dafür, nur Warnungen zu verarbeiten, die eine Schriftartersetzung sind, und geben die Warnung auf dem Bildschirm aus. Das folgende Beispiel zeigt, wie Sie Benachrichtigungen über Schriftersetzungen erhalten, indem Sie verwenden[IWarnungRückruf](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback).

**C#**

{{< highlight "java" >}}

 // The path to the documents directory.

string dataDir = RunExamples.GetDataDir_Intro();

// load the document to render.

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// initialize PdfSaveOptions object

PdfSaveOptions saveOp = new PdfSaveOptions();

// create a new class implementing IWarningCallback which collect any warnings produced during drawing save.

HandleDocumentWarnings callback = new HandleDocumentWarnings();

saveOp.WarningCallback = callback;

// pass the save options along with the save path to the save method.

diagram.Save(dataDir + "NotificationofMissingFonts_Out.pdf", saveOp);

{{< /highlight >}}
#### **Implementieren des IWarningCallback**
Der letzte Schritt besteht darin, die Klasse zu erstellen, die die implementiert[IWarnungRückruf](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback)Schnittstelle. Diese Klasse gibt alle Warnungen zur Schriftartersetzung an die Konsole aus. Das folgende Beispiel zeigt, wie IWarningCallback implementiert wird, um beim Speichern des Dokuments über jede Schriftartersetzung benachrichtigt zu werden.

**C#**

{{< highlight "java" >}}

 class HandleDocumentWarnings : IWarningCallback

{

    /**

    * Our callback only needs to implement the "Warning" method. This method is

    * called whenever there is a potential issue during document processing.

    * The callback can be set to listen for warnings generated during document

    * load and/or document save.

    */

    public void Warning(WarningInfo info)

    {

        // We are only interested in fonts being substituted.

        if (info.WarningType == WarningType.FontSubstitution)

        {

            Console.WriteLine("Font substitution: " + info.Description);

        }

    }

}

{{< /highlight >}}
