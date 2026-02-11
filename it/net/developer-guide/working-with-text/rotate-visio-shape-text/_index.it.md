---
title: Ruota Visio Forma testo
type: docs
weight: 9
url: /it/net/rotate-visio-shape-text/
keywords: Rotate, visio, Tex
description: Come ruotare il testo della forma in visio utilizzando .NET Diagram API.
---
## **Creazione di un numero Diagram**
 Aspose.Diagram for .NET consente di leggere e creare Microsoft Visio diagrammi dall'interno delle proprie applicazioni, senza Microsoft Office Automazione. Il primo passaggio durante la creazione di nuovi documenti è creare un numero diagram. Quindi[aggiungere forme e connettori](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)per creare diagram. Utilizzare il costruttore predefinito di[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class per creare un nuovo diagram.
### **Esempio di programmazione**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Create directory if it is not already present.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Initialize a new Visio
Diagram diagram = new Diagram();
dataDir = dataDir + "CreateDiagram_out.vsdx";
// Save in the VSDX format
diagram.Save(dataDir, SaveFileFormat.VSDX);

{{< /highlight >}}


Questo esempio funziona come segue:

1. Creare un oggetto della classe Diagram.
1. Ottieni una pagina particolare
1. Ottieni una forma particolare
1. Ottieni il testo Forma e ruota il testo
1. Chiama il metodo Save dell'oggetto classe Diagram e passa anche il percorso file completo e l'oggetto DiagramSaveOptions.
### **Ruota il testo Esempio di programmazione**
Il seguente codice di esempio mostra come ruotare il testo nel Visio diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ShapeText();

// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "UpdateShapeText.vsd");
// Get page by name
Page page = diagram.Pages.GetPage("Flow 1");
// Find a particular shape and update its text
foreach (Aspose.Diagram.Shape shape in page.Shapes)
{
    if (shape.NameU.ToLower() == "process" && shape.ID == 1)
    {
        shape.Text.Value.Clear();
        shape.Text.Value.Add(new Txt("New Text"));
        // Set orientation angle
        double angleDeg = 90;
        double angleRad = (Math.PI / 180) * angleDeg;
        shape.TextXForm.TxtAngle.Value = angleRad;
    }
}
// Save diagram
diagram.Save(dataDir + "UpdateShapeText_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

