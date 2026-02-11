---
title: Arbeiten mit SolutionXML-Elementen
type: docs
weight: 140
url: /de/java/working-with-solutionxml-elements/
---
## **Fügen Sie SolutionXML-Element zur Zeichnung Visio hinzu**
 SolutionXML ist wohlgeformtes XML, das in einem SolutionXML-Element enthalten ist, das ein standardisiertes Mittel zum Beibehalten von Lösungsdaten bereitstellt. Benutzer können SolutionXML auf Dokumentebene speichern, wo es sofort im VisioDocument-Element gespeichert wird. In der Regel ist dies die einfachste Methode zum Speichern und Abrufen von SolutionXML[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

 Das[LösungXML](https://reference.aspose.com/diagram/java/com.aspose.diagram/SolutionXML) Die Klasse stellt das SolutionXML-Element in Visio-Zeichnungen dar. Die Add-Methode, verfügbar gemacht durch die[LösungXML](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/SolutionXML) -Klasse ermöglicht das Hinzufügen eines SolutionXML-Elements.
### **Programmierbeispiel für SolutionXML-Elemente hinzufügen**
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
## **Lesen von XML-Werten aus dem SolutionXML-Element**
SolutionXML ist wohlgeformtes XML, das in einem SolutionXML-Element enthalten ist, das ein standardisiertes Mittel zum Beibehalten von Lösungsdaten bereitstellt. Die Benutzer können mithilfe von XML-Werte aus dem SolutionXML-Element lesen[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

 Die SolutionXMLs-Eigenschaft, die von der bereitgestellt wird[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) Klasse, unterstützt eine Sammlung von Aspose.Diagram.SolutionXML-Objekten. Mit dieser Eigenschaft können die XML-Werte aus dem SolutionXML-Element gelesen werden.
### **Programmierbeispiel für SolutionXML-Elemente lesen**
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
