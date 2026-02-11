---
title: Arbeiten mit SolutionXML-Elementen
type: docs
weight: 110
url: /de/net/working-with-solutionxml-elements/
description: In diesem Abschnitt wird erläutert, wie Sie solutionXml hinzufügen oder XML-Werte aus dem solutionXml-Element mit Aspose.Diagram abrufen.
---
## **Fügen Sie SolutionXML-Element zur Zeichnung Visio hinzu**
 SolutionXML ist wohlgeformtes XML, das in einem SolutionXML-Element enthalten ist, das ein standardisiertes Mittel zum Beibehalten von Lösungsdaten bereitstellt. Benutzer können SolutionXML auf Dokumentebene speichern, wo es sofort im VisioDocument-Element gespeichert wird. In der Regel ist dies die einfachste Methode zum Speichern und Abrufen von SolutionXML[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 Das[LösungXML](http://www.aspose.com/api/net/diagram/aspose.diagram/solutionXML) Die Klasse stellt das SolutionXML-Element in Visio-Zeichnungen dar. Die Add-Methode, verfügbar gemacht durch die[LösungXML](http://www.aspose.com/api/net/diagram/aspose.diagram/solutionXML) -Klasse ermöglicht das Hinzufügen eines SolutionXML-Elements.
### **Programmierbeispiel für SolutionXML-Elemente hinzufügen**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_SolutionXML();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Initialize SolutionXML object
SolutionXML solXML = new SolutionXML();
// Set name
solXML.Name = "Solution XML";
// Set xml value
solXML.XmlValue = "XML Value";
// Add SolutionXML element
diagram.SolutionXMLs.Add(solXML);

// Save Visio diagram
diagram.Save(dataDir + "AddSolutionXMLElement_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Lesen von XML-Werten aus dem SolutionXML-Element**
SolutionXML ist wohlgeformtes XML, das in einem SolutionXML-Element enthalten ist, das ein standardisiertes Mittel zum Beibehalten von Lösungsdaten bereitstellt. Die Benutzer können mithilfe von XML-Werte aus dem SolutionXML-Element lesen[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 Die SolutionXMLs-Eigenschaft, die von der bereitgestellt wird[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Klasse, unterstützt eine Sammlung von Aspose.Diagram.SolutionXML-Objekten. Mit dieser Eigenschaft können die XML-Werte aus dem SolutionXML-Element gelesen werden.
### **Programmierbeispiel für SolutionXML-Elemente lesen**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_SolutionXML();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Iterate through SolutionXML elements
foreach (SolutionXML solutionXML in diagram.SolutionXMLs)
{
    // Get name property
    Console.WriteLine(solutionXML.Name);
    // Get xml value
    Console.WriteLine(solutionXML.XmlValue);
}

{{< /highlight >}}

