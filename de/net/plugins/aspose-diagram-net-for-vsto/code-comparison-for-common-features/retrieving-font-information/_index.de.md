---
title: Abrufen von Schriftinformationen
type: docs
weight: 80
url: /de/net/retrieving-font-information/
---
## **VSTO**
Unten ist der Code zum Abrufen von Schriftartinformationen:

{{< highlight "cs" >}}

  foreach (Font font in Application.ActiveDocument.Fonts)

 {

    //Display information about the fonts

    MessageBox.Show(font.Name);

 }

{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

 Aspose.Diagram verfügt über Mechanismen zum Abrufen von Informationen über die Elemente, aus denen diagram besteht[Seiten](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) , Schablonen,[Anschlüsse](/diagram/de/net/retrieving-connector-information/)und auch Schriftarten. Dieser Artikel zeigt, wie Sie herausfinden, welche Schriftarten in einer diagram verwendet werden.

{{% /alert %}} 

 Das[Schriftart](https://reference.aspose.com/diagram/net/aspose.diagram/font) Objekt stellt eine Schriftart dar, die entweder auf Text in einem Dokument angewendet wird oder zur Verwendung auf dem System verfügbar ist.

Ein Font-Objekt ordnet einen Namen (z. B. „Arial“) der Schriftart-ID (z. B. 3) zu, die Microsoft Visio in einer Font-Zelle in einem Zeichenabschnitt einer Form speichert, die mit dieser Schriftart formatierten Text enthält. Schriftart-IDs können sich ändern, wenn ein Dokument auf verschiedenen Systemen geöffnet wird oder wenn Schriftarten installiert oder entfernt werden.

{{< highlight "cs" >}}

  //Call the diagram constructor to load diagram from a VDX file

 Diagram vdxDiagram = new Diagram(@"E:\Aspose\Aspose Vs VSTO\Aspose.Diagram Vs VSTO Visio v1.1\Sample Files\Drawing1.vdx");

 foreach (Aspose.Diagram.Font font in vdxDiagram.Fonts)

 {

    //Display information about the fonts

    Console.WriteLine(font.Name);

 }

{{< /highlight >}}
## **Beispielcode herunterladen**
- [GitHub](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Laufcode herunterladen**
- [GitHub](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Retrieving%20Font%20Information)
