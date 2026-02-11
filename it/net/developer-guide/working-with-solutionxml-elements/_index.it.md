---
title: Lavorare con gli elementi SolutionXML
type: docs
weight: 110
url: /it/net/working-with-solutionxml-elements/
description: Questa sezione spiega come aggiungere solutionXml o ottenere valori xml dall'elemento solutionXml con Aspose.Diagram.
---
## **Aggiungere l'elemento SolutionXML al disegno Visio**
 SolutionXML è un codice XML ben formato contenuto all'interno di un elemento SolutionXML che fornisce un mezzo standardizzato per la persistenza dei dati della soluzione. Gli utenti possono archiviare SolutionXML a livello di documento, dove viene archiviato immediatamente nell'elemento VisioDocument. In genere, questo è il modo più semplice per archiviare e recuperare SolutionXML utilizzando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 Il[SoluzioneXML](http://www.aspose.com/api/net/diagram/aspose.diagram/solutionXML) class rappresenta l'elemento SolutionXML nei disegni Visio. Il metodo Add, esposto da[SoluzioneXML](http://www.aspose.com/api/net/diagram/aspose.diagram/solutionXML) class, consente di aggiungere un elemento SolutionXML.
### **Aggiungere un esempio di programmazione dell'elemento SolutionXML**

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

## **Lettura di valori XML dall'elemento SolutionXML**
SolutionXML è un codice XML ben formato contenuto all'interno di un elemento SolutionXML che fornisce un mezzo standardizzato per la persistenza dei dati della soluzione. Gli utenti possono leggere i valori XML dall'elemento SolutionXML utilizzando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 La proprietà SolutionXMLs, esposta da[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class, supporta una raccolta di oggetti Aspose.Diagram.SolutionXML. Questa proprietà può essere utilizzata per leggere i valori XML dall'elemento SolutionXML.
### **Lettura dell'esempio di programmazione dell'elemento SolutionXML**

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

