---
title: Trabajar con elementos SolutionXML
type: docs
weight: 140
url: /es/java/working-with-solutionxml-elements/
---
## **Agregue el elemento SolutionXML al dibujo Visio**
 SolutionXML es un XML bien formado contenido dentro de un elemento SolutionXML que proporciona un medio estandarizado para conservar los datos de la solución. Los usuarios pueden almacenar SolutionXML en el nivel de documento, donde se almacena inmediatamente en el elemento VisioDocument. Por lo general, esta es la forma más fácil de almacenar y recuperar SolutionXML usando[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

 los[SoluciónXML](https://reference.aspose.com/diagram/java/com.aspose.diagram/SolutionXML) La clase representa el elemento SolutionXML en los dibujos Visio. El método Add, expuesto por el[SoluciónXML](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/SolutionXML) clase, permite agregar un elemento SolutionXML.
### **Agregar muestra de programación de elemento SolutionXML**
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
## **Lectura de valores XML del elemento SolutionXML**
SolutionXML es un XML bien formado contenido dentro de un elemento SolutionXML que proporciona un medio estandarizado para conservar los datos de la solución. Los usuarios pueden leer valores XML del elemento SolutionXML usando[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

 La propiedad SolutionXMLs, expuesta por el[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) clase, admite una colección de objetos Aspose.Diagram.SolutionXML. Esta propiedad se puede utilizar para leer los valores XML del elemento SolutionXML.
### **Ejemplo de programación de elementos de Reading SolutionXML**
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
