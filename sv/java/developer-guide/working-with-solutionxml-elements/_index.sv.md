---
title: Arbeta med SolutionXML Elements
type: docs
weight: 140
url: /sv/java/working-with-solutionxml-elements/
---
## **Lägg till SolutionXML Element till Visio-ritningen**
 SolutionXML är välformaterad XML som ingår i ett SolutionXML-element som tillhandahåller ett standardiserat sätt att bevara lösningsdata. Användare kan lagra SolutionXML på dokumentnivå, där det lagras omedelbart i VisioDocument-elementet. Vanligtvis är detta det enklaste sättet att lagra och hämta SolutionXML med hjälp av[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

 De[SolutionXML](https://reference.aspose.com/diagram/java/com.aspose.diagram/SolutionXML) klass representerar SolutionXML-elementet i Visio-ritningar. Add-metoden, exponerad av[SolutionXML](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/SolutionXML) klass, gör det möjligt att lägga till ett SolutionXML-element.
### **Lägg till SolutionXML Element Programmeringsexempel**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddSolutionXMLElement.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// initialize SolutionXML object
SolutionXML solXML = new SolutionXML();
// set name
solXML.setName("Solution XML");
// set xml value
solXML.setXmlValue("XML Value");
// add SolutionXML element
diagram.getSolutionXMLs().add(solXML);

// save Visio diagram
diagram.save(dataDir + "AddSolutionXMLElement_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Läser XML-värden från SolutionXML-elementet**
SolutionXML är välformaterad XML som ingår i ett SolutionXML-element som tillhandahåller ett standardiserat sätt att bevara lösningsdata. Användarna kan läsa XML-värden från SolutionXML-elementet med hjälp av[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

 SolutionXMLs-egenskapen, exponerad av[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) klass, stöder en samling Aspose.Diagram.SolutionXML-objekt. Den här egenskapen kan användas för att läsa XML-värdena från SolutionXML-elementet.
### **Läser SolutionXML Element Programmeringsexempel**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadSolutionXMLElement.class);   
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// iterate through SolutionXML elements
for (SolutionXML solutionXML :(Iterable<SolutionXML>) diagram.getSolutionXMLs())
{
    // get name property
    System.out.println(solutionXML.getName());
    // get xml value
    System.out.println(solutionXML.getXmlValue());
}

{{< /highlight >}}
```
