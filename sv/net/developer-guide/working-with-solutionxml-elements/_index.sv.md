---
title: Arbeta med SolutionXML Elements
type: docs
weight: 110
url: /sv/net/working-with-solutionxml-elements/
description: Det här avsnittet förklarar hur man lägger till solutionXml eller får xml-värden från solutionXml-elementet med Aspose.Diagram.
---
## **Lägg till SolutionXML Element till Visio-ritningen**
 SolutionXML är välformaterad XML som ingår i ett SolutionXML-element som tillhandahåller ett standardiserat sätt att bevara lösningsdata. Användare kan lagra SolutionXML på dokumentnivå, där det lagras omedelbart i VisioDocument-elementet. Vanligtvis är detta det enklaste sättet att lagra och hämta SolutionXML med hjälp av[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 De[SolutionXML](http://www.aspose.com/api/net/diagram/aspose.diagram/solutionXML) klass representerar SolutionXML-elementet i Visio-ritningar. Add-metoden, exponerad av[SolutionXML](http://www.aspose.com/api/net/diagram/aspose.diagram/solutionXML) klass, gör det möjligt att lägga till ett SolutionXML-element.
### **Lägg till SolutionXML Element Programmeringsexempel**
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
## **Läser XML-värden från SolutionXML-elementet**
SolutionXML är välformaterad XML som ingår i ett SolutionXML-element som tillhandahåller ett standardiserat sätt att bevara lösningsdata. Användarna kan läsa XML-värden från SolutionXML-elementet med hjälp av[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 SolutionXMLs-egenskapen, exponerad av[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) klass, stöder en samling Aspose.Diagram.SolutionXML-objekt. Den här egenskapen kan användas för att läsa XML-värdena från SolutionXML-elementet.
### **Läser SolutionXML Element Programmeringsexempel**
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
