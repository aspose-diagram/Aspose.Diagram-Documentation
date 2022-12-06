---
title: Dokumentzusammenfassung schreiben
type: docs
weight: 70
url: /de/net/writing-document-summary/
---
## **VSTO**
Unten ist der Code zum Schreiben der Dokumentzusammenfassung von Visio:

{{< highlight "cs" >}}

  Application.ActiveDocument.Creator = "Zeeshan";

 Application.ActiveDocument.Company = "Aspose";

 Application.ActiveDocument.Category = "Drawing 2D";

 Application.ActiveDocument.Manager = "Self";

 Application.ActiveDocument.Title = "Zeeshan";

 Application.ActiveDocument.Subject = "Visio Diagram";


{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

Mit Microsoft Visio können Sie eine Reihe von zusammenfassenden Informationseigenschaften für Dokumente definieren, die Ihnen und Ihren Kollegen helfen, eine diagram zu identifizieren. Zusammenfassende Eigenschaften, z. B. Titel, Betreff, Autor und Beschreibung, erleichtern das Auffinden der Datei bei der Suche und die Erkennung beim Durchsuchen Dateien.

{{% /alert %}} 
### **Schreiben Microsoft Visio Document Summary Info**
 Das[Dokumenteigenschaften](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties)-Klasse stellt eine Reihe von Eigenschaften bereit, um die zusammenfassenden Informationen von Microsoft Visio diagram festzulegen oder abzurufen. Aspose.Diagram for .NET kann die Zeichnungszusammenfassungsinformationen aktualisieren und dann die Zeichnungsdatei zurück zu VDX schreiben.

So aktualisieren Sie die Zeichnungszusammenfassungsinformationen einer vorhandenen VDX- oder VSD-Datei:

1.  Erstellen Sie eine Instanz der[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram) Klasse.
1. Legen Sie Eigenschaften fest, die von Diagram.DocumentProps bereitgestellt werden, um die zusammenfassenden Informationen für die Zeichnungsdatei Visio zu definieren.
1. Rufen Sie die Save-Methode der Klasse Diagram auf, um die Zeichnungsdatei Visio in VDX zu schreiben.

Überprüfen Sie die zusammenfassenden Informationen:

1. Öffnen Sie die Ausgabedatei VDX in Microsoft Visio.
1.  Auswählen**Die Info** von dem**Datei** Speisekarte.

{{< highlight "cs" >}}

  //Call the diagram constructor to load diagram from a VDX file

 Diagram vdxDiagram = new Diagram("Drawing1.vdx");

 //Set some summary information about the diagram

 vdxDiagram.DocumentProps.Creator = "Ijaz";

 vdxDiagram.DocumentProps.Company = "Aspose";

 vdxDiagram.DocumentProps.Category = "Drawing 2D";

 vdxDiagram.DocumentProps.Manager = "Sergey Polshkov";

 vdxDiagram.DocumentProps.Title = "Aspose Title";

 vdxDiagram.DocumentProps.TimeCreated = DateTime.Now;

 vdxDiagram.DocumentProps.Subject = "Visio Diagram";

 vdxDiagram.DocumentProps.Template = "Aspose Template";

 //Write the updated file to the disk in VDX file format

 vdxDiagram.Save("output.vdx", SaveFileFormat.VDX);


{{< /highlight >}}
## **Beispielcode herunterladen**
- [GitHub](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Laufcode herunterladen**
- [GitHub](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Writing%20Document%20Summary)
