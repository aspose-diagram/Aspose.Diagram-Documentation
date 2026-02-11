---
title: Working with SolutionXML Elements
type: docs
weight: 110
url: /net/working-with-solutionxml-elements/
description: This section explains how to  add solutionXml or get xml values from solutionXml element with Aspose.Diagram.
---

## **Add SolutionXML Element to the Visio Drawing**
SolutionXML is well-formed XML contained within a SolutionXML element that provides a standardized means of persisting solution data. Users may store SolutionXML at the Document level, where it is stored immediately in the VisioDocument element. Typically, this is the easiest way to store and retrieve SolutionXML using [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

The [SolutionXML](http://www.aspose.com/api/net/diagram/aspose.diagram/solutionXML) class represents SolutionXML element in Visio drawings. The Add method, exposed by the [SolutionXML](http://www.aspose.com/api/net/diagram/aspose.diagram/solutionXML) class, allows adding a SolutionXML element.
### **Add SolutionXML Element Programming Sample**

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

## **Reading XML Values from the SolutionXML Element**
SolutionXML is well-formed XML contained within a SolutionXML element that provides a standardized means of persisting solution data. The users can read XML values from the SolutionXML element using [Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

The SolutionXMLs property, exposed by the [Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class, supports a collection of Aspose.Diagram.SolutionXML objects. This property can be used to read the XML values from the SolutionXML element.
### **Reading SolutionXML Element Programming Sample**

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

