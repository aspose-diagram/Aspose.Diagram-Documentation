---
title: Aspose.Diagram Font-Operationen
type: docs
weight: 170
url: /de/java/aspose-diagram-font-operations/
---
{{% alert color="primary" %}} 

Mit Aspose.Diagram können Entwickler die Schriftverzeichnisse zum Rendern in Visio-Diagrammen festlegen. Dieser Artikel zeigt, wie Sie Schriftarten aus benutzerdefinierten Verzeichnissen verwenden.

{{% /alert %}} 
### **Arbeiten mit Schriftarten**
#### **Wobei Aspose.Diagram auf Windows nach TrueType-Schriftarten sucht**
 Aspose.Diagram sucht nach Schriften in der**Windows\Schriftarten** Mappe. Diese Standardeinstellung funktioniert die meiste Zeit, also geben Sie Ihre eigenen Schriftartenordner nur dann an, wenn Sie es wirklich brauchen.
#### **So geben Sie einen Schriftordner explizit an**
 Aspose.Diagram APIs haben die setFontDirs-Methode für die verfügbar gemacht[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) -Klasse, um die Schriftordner wie unten beschrieben anzugeben.

1. Die Methode Diagram.setFontDirs verwendet ein String-Array als Parameter, sodass Entwickler mit diesem Ansatz viele Schriftartverzeichnisse angeben können.

{{% alert color="primary" %}} 

Wenn Sie den Schriftartenordner mit dem oben genannten Ansatz angeben, empfehlen wir, den Speicherort der Schriftart am Anfang der Anwendung festzulegen, da Sie sonst möglicherweise schlecht formatierte Ergebnisse erhalten.

{{% /alert %}} {{% alert color="primary" %}} 

Das Festlegen des Schriftartenordners mit einer der oben genannten Methoden stellt nicht sicher, dass der Aspose.Diagram API nicht nach den Schriftarten an Standardspeicherorten wie dem Schriftartenordner des Systems sucht.

{{% /alert %}} 

Veranschaulicht, wie Aspose.Diagram so eingestellt wird, dass beim Rendern oder Einbetten von Schriftarten in mehreren Ordnern nach TrueType-Schriftarten gesucht wird.
#### **Programmierbeispiel**
Das folgende Codebeispiel zeigt, wie Sie Aspose.Diagram so einstellen, dass es beim Rendern oder Einbetten von Schriftarten in mehreren Ordnern nach TrueType-Schriftarten sucht.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SpecifyFontLocation.class);    

String[] fontDirs = new String[] { "C:\\MyFonts\\", "D:\\Misc\\Fonts\\" };
//Load the Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
//setting the custom font directories
diagram.setFontDirs(fontDirs);

//saving Visio diagram in PDF format
diagram.save(dataDir + "SetFontsFolders_Out.pdf", SaveFileFormat.PDF);

{{< /highlight >}}

### **Erhalten Sie während des Renderns eine Benachrichtigung über fehlende Schriften und Schriftersetzungen**
Aspose.Diagram API requires access to the accurate font in order to properly render the drawing to PDF format. If the required font is not available on the machine, then Aspose.Diagram API renders any instance of that font using the default font or the closest available font on the machine, since this substitution can change the look of the rendered drawing, developers may need to be notified when a font is missing and with what font it will be replaced.
#### **Programmierbeispiel für Benachrichtigung über fehlende Schriftarten und Schriftartersetzung**
Um während des Renderns über die Ersetzung von Schriftarten benachrichtigt zu werden:

1. Erstellen Sie eine Klasse, die die implementiert[IWarnungRückruf](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)
1. Übergeben Sie es an die Eigenschaft PdfSaveOptions.setWarningCallback(com.aspose.diagram.IWarningCallback).

Beim Speichern der Zeichnung wird die Instanz von[IWarnungRückruf](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)wird aufgerufen, wenn es potenzielle Genauigkeitsprobleme mit der Zeichnung gibt. In diesem Fall entscheiden wir uns dafür, nur Warnungen zu verarbeiten, die eine Schriftartersetzung sind, und geben die Warnung auf dem Bildschirm aus. Das folgende Beispiel zeigt, wie Sie Benachrichtigungen über Schriftersetzungen erhalten, indem Sie verwenden[IWarnungRückruf](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback).

**Java**

{{< highlight "java" >}}

 // load the document to render.

Diagram diagram = new Diagram("C:\\temp\\Output.vsdx");


// initialize PdfSaveOptions object

com.aspose.diagram.PdfSaveOptions saveOp = new com.aspose.diagram.PdfSaveOptions();

// create a new class implementing IWarningCallback which collect any warnings produced during drawing save.

HandleDocumentWarnings callback = new HandleDocumentWarnings();

saveOp.setWarningCallback(callback);



// pass the save options along with the save path to the save method.

diagram.save("C:\\temp\\Rendering.MissingFontNotification Out.pdf", saveOp);

{{< /highlight >}}
#### **Implementieren des IWarningCallback**
Der letzte Schritt besteht darin, die Klasse zu erstellen, die die implementiert[IWarnungRückruf](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)Schnittstelle. Diese Klasse gibt alle Warnungen zur Schriftartersetzung an die Konsole aus. Das folgende Beispiel zeigt, wie IWarningCallback implementiert wird, um beim Speichern des Dokuments über jede Schriftartersetzung benachrichtigt zu werden.



**Java**

{{< highlight "java" >}}

 public class HandleDocumentWarnings implements IWarningCallback {

     /**

     * Our callback only needs to implement the "Warning" method. This method is

     * called whenever there is a potential issue during document processing.

     * The callback can be set to listen for warnings generated during document

     * load and/or document save.

     */

     public void warning(WarningInfo info) {

         // We are only interested in fonts being substituted.

         if (info.getWarningType() == WarningType.FONT_SUBSTITUTION) {

         System.out.println("Font substitution: " + info.getDescription());

     }

 }

}

{{< /highlight >}}
