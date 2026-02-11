---
title: Utilisation des éléments SolutionXML
type: docs
weight: 140
url: /fr/java/working-with-solutionxml-elements/
---
## **Ajouter un élément SolutionXML au dessin Visio**
 SolutionXML est un XML bien formé contenu dans un élément SolutionXML qui fournit un moyen standardisé de persistance des données de solution. Les utilisateurs peuvent stocker SolutionXML au niveau du document, où il est stocké immédiatement dans l'élément VisioDocument. En règle générale, il s'agit du moyen le plus simple de stocker et de récupérer SolutionXML à l'aide de[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

 La[SolutionXML](https://reference.aspose.com/diagram/java/com.aspose.diagram/SolutionXML) La classe représente l'élément SolutionXML dans les dessins Visio. La méthode Add, exposée par le[SolutionXML](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/SolutionXML) class, permet d'ajouter un élément SolutionXML.
### **Ajouter un exemple de programmation d'élément SolutionXML**
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
## **Lecture des valeurs XML à partir de l'élément SolutionXML**
SolutionXML est un XML bien formé contenu dans un élément SolutionXML qui fournit un moyen standardisé de persistance des données de solution. Les utilisateurs peuvent lire les valeurs XML de l'élément SolutionXML en utilisant[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

 La propriété SolutionXMLs, exposée par le[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) classe, prend en charge une collection d'objets Aspose.Diagram.SolutionXML. Cette propriété peut être utilisée pour lire les valeurs XML à partir de l'élément SolutionXML.
### **Lecture de l'exemple de programmation d'éléments SolutionXML**
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
