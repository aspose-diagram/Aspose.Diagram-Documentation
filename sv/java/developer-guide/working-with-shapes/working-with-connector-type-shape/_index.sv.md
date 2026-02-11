---
title: Arbeta med Connector Type Shape
type: docs
weight: 80
url: /sv/java/working-with-connector-type-shape/
---
## **Ställ in utseendet på kontakttypsformen i Visio**
Det här ämnet utvecklar hur utvecklare kan ändra utseendet på formen av dynamisk kontakttyp med hjälp av Aspose.Diagram for Java.
### **Ställ in kontaktens utseende**
 SetConnectorsType-metoden exponerad av[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) klass kan användas för att ställa in utseendet på kontakttypens form.

Koden nedan visar hur man:

1. Ladda ett prov diagram.
1. skaffa en viss sida.
1. få en speciell kontaktform.
1. ställ in formens utseende.
1. spara diagram
#### **Ställ in kontaktens utseende Programmeringsexempel**
Använd följande kod i din Java-applikation för att ställa in utseendet på kontakttypens form med Aspose.Diagram for Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetConnectorAppearance.class);  
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//get a particular page
Page page = diagram.getPages().getPage("Page-3");
//get a dynamic connector type shape by id
Shape shape = page.getShapes().getShape(18);
// set dynamic connector appearance
shape.setConnectorsType(ConnectorsTypeValue.STRAIGHT_LINES);

//saving Visio diagram
diagram.save(dataDir + "SetConnectorAppearance_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Välj Omdirigeringsalternativ för Connector Shape**
 ConFixedCode-egenskapen exponerad av[Layout](https://reference.aspose.com/diagram/java/com.aspose.diagram/layout) klass kan användas för att välja omdirigeringsalternativ. Layout-egenskapen, exponerad av[Form](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) klass, kommer att användas.

|<p>**Hur man väljer omdirigeringsalternativ** </p><p>![todo:image_alt_text](http://i.imgur.com/1O70sSA.png)</p>|
|:- |
Koden nedan visar hur man:

1. Ladda en exempelfil.
1. skaffa en viss sida.
1. få en speciell kontaktform.
1. ställ in alternativ för omdirigering.
1. spara diagram.
### **Välj Programmeringsexempel för omdirigeringsalternativ**
Använd följande kod i din Java-applikation för att välja omdirigeringsalternativet för kontaktformen med Aspose.Diagram for Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RerouteConnectors.class);   
// call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-3");

// get a particular connector shape
Shape shape = page.getShapes().getShape(18);
// set reroute option
shape.getLayout().getConFixedCode().setValue(ConFixedCodeValue.NEVER_REROUTE);

// save Visio diagram
diagram.save(dataDir + "RerouteConnectors_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
