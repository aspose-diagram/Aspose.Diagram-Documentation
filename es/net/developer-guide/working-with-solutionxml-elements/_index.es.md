---
title: Trabajar con elementos SolutionXML
type: docs
weight: 110
url: /es/net/working-with-solutionxml-elements/
description: Esta sección explica cómo agregar solutionXml u obtener valores xml del elemento solutionXml con Aspose.Diagram.
---
## **Agregue el elemento SolutionXML al dibujo Visio**
 SolutionXML es un XML bien formado contenido dentro de un elemento SolutionXML que proporciona un medio estandarizado para conservar los datos de la solución. Los usuarios pueden almacenar SolutionXML en el nivel de documento, donde se almacena inmediatamente en el elemento VisioDocument. Por lo general, esta es la forma más fácil de almacenar y recuperar SolutionXML usando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 los[SoluciónXML](http://www.aspose.com/api/net/diagram/aspose.diagram/solutionXML) La clase representa el elemento SolutionXML en los dibujos Visio. El método Add, expuesto por el[SoluciónXML](http://www.aspose.com/api/net/diagram/aspose.diagram/solutionXML) clase, permite agregar un elemento SolutionXML.
### **Agregar muestra de programación de elemento SolutionXML**

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

## **Lectura de valores XML del elemento SolutionXML**
SolutionXML es un XML bien formado contenido dentro de un elemento SolutionXML que proporciona un medio estandarizado para conservar los datos de la solución. Los usuarios pueden leer valores XML del elemento SolutionXML usando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 La propiedad SolutionXMLs, expuesta por el[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) clase, admite una colección de objetos Aspose.Diagram.SolutionXML. Esta propiedad se puede utilizar para leer los valores XML del elemento SolutionXML.
### **Ejemplo de programación de elementos de Reading SolutionXML**

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

