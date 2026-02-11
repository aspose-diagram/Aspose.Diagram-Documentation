---
title: Utilisation des éléments SolutionXML
type: docs
weight: 110
url: /fr/net/working-with-solutionxml-elements/
description: Cette section explique comment ajouter solutionXml ou obtenir des valeurs xml à partir de l'élément solutionXml avec Aspose.Diagram.
---
## **Ajouter un élément SolutionXML au dessin Visio**
 SolutionXML est un XML bien formé contenu dans un élément SolutionXML qui fournit un moyen standardisé de persistance des données de solution. Les utilisateurs peuvent stocker SolutionXML au niveau du document, où il est stocké immédiatement dans l'élément VisioDocument. En règle générale, il s'agit du moyen le plus simple de stocker et de récupérer SolutionXML à l'aide de[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 La[SolutionXML](http://www.aspose.com/api/net/diagram/aspose.diagram/solutionXML) La classe représente l'élément SolutionXML dans les dessins Visio. La méthode Add, exposée par le[SolutionXML](http://www.aspose.com/api/net/diagram/aspose.diagram/solutionXML) class, permet d'ajouter un élément SolutionXML.
### **Ajouter un exemple de programmation d'élément SolutionXML**
```
{{< highlight "csharp" >}}
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
```
## **Lecture des valeurs XML à partir de l'élément SolutionXML**
SolutionXML est un XML bien formé contenu dans un élément SolutionXML qui fournit un moyen standardisé de persistance des données de solution. Les utilisateurs peuvent lire les valeurs XML de l'élément SolutionXML en utilisant[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 La propriété SolutionXMLs, exposée par le[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) classe, prend en charge une collection d'objets Aspose.Diagram.SolutionXML. Cette propriété peut être utilisée pour lire les valeurs XML à partir de l'élément SolutionXML.
### **Lecture de l'exemple de programmation d'éléments SolutionXML**
```
{{< highlight "csharp" >}}
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
```
