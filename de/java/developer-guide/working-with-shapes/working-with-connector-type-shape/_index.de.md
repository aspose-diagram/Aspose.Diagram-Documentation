---
title: Arbeiten mit Konnektortyp-Shape
type: docs
weight: 80
url: /de/java/working-with-connector-type-shape/
---
## **Legen Sie das Erscheinungsbild der Verbindertypform in Visio fest**
In diesem Thema wird erläutert, wie Entwickler das Erscheinungsbild der Form des dynamischen Verbindungstyps mithilfe von Aspose.Diagram for Java ändern können.
### **Legen Sie das Erscheinungsbild des Verbinders fest**
 Die SetConnectorsType-Methode, die von der bereitgestellt wird[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) -Klasse kann verwendet werden, um das Erscheinungsbild der Verbindertypform festzulegen.

Der folgende Code zeigt, wie man:

1. Laden Sie eine Probe diagram.
1. eine bestimmte Seite bekommen.
1. erhalten Sie eine bestimmte Steckerform.
1. Erscheinungsbild der Form festlegen.
1. außer diagram
#### **Programmierbeispiel für das Aussehen des Konnektors festlegen**
Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um das Aussehen der Verbindertypform mithilfe von Aspose.Diagram for Java festzulegen.


{{< highlight java >}}
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

## **Wählen Sie die Umleitungsoption der Verbindungsform aus**
 Die ConFixedCode-Eigenschaft, die von der bereitgestellt wird[Layout](https://reference.aspose.com/diagram/java/com.aspose.diagram/layout) Klasse kann verwendet werden, um die Umleitungsoption auszuwählen. Die Layout-Eigenschaft, verfügbar gemacht durch die[Form](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/shape) Klasse, verwendet werden.

|<p>**So wählen Sie Umleitungsoptionen aus** </p><p>![todo: Bild_alt_Text](http://i.imgur.com/1O70sSA.png)</p>|
|:- |
Der folgende Code zeigt, wie man:

1. Laden Sie eine Beispieldatei.
1. eine bestimmte Seite bekommen.
1. erhalten Sie eine bestimmte Steckerform.
1. Umleitungsoptionen festlegen.
1. außer diagram.
### **Wählen Sie Programmierbeispiel für Umleitungsoption**
Verwenden Sie den folgenden Code in Ihrer Java-Anwendung, um die Umleitungsoption der Verbinderform mit Aspose.Diagram for Java auszuwählen.


{{< highlight java >}}
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

