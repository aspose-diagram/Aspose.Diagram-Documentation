---
title: Lavorare con gli elementi SolutionXML
type: docs
weight: 140
url: /it/java/working-with-solutionxml-elements/
---
## **Aggiungere l'elemento SolutionXML al disegno Visio**
 SolutionXML è un codice XML ben formato contenuto all'interno di un elemento SolutionXML che fornisce un mezzo standardizzato per la persistenza dei dati della soluzione. Gli utenti possono archiviare SolutionXML a livello di documento, dove viene archiviato immediatamente nell'elemento VisioDocument. In genere, questo è il modo più semplice per archiviare e recuperare SolutionXML utilizzando[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

 Il[SoluzioneXML](https://reference.aspose.com/diagram/java/com.aspose.diagram/SolutionXML) class rappresenta l'elemento SolutionXML nei disegni Visio. Il metodo Add, esposto da[SoluzioneXML](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/SolutionXML) class, consente di aggiungere un elemento SolutionXML.
### **Aggiungere un esempio di programmazione dell'elemento SolutionXML**
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
## **Lettura di valori XML dall'elemento SolutionXML**
SolutionXML è un codice XML ben formato contenuto all'interno di un elemento SolutionXML che fornisce un mezzo standardizzato per la persistenza dei dati della soluzione. Gli utenti possono leggere i valori XML dall'elemento SolutionXML utilizzando[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

 La proprietà SolutionXMLs, esposta da[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class, supporta una raccolta di oggetti Aspose.Diagram.SolutionXML. Questa proprietà può essere utilizzata per leggere i valori XML dall'elemento SolutionXML.
### **Lettura dell'esempio di programmazione dell'elemento SolutionXML**
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
