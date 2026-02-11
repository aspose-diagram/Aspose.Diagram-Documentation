---
title: Arbeiten mit Hyperlinks
type: docs
weight: 110
url: /de/java/working-with-hyperlinks/
---
## **Hyperlink zu einer Visio-Form hinzufügen**
Es ist ein einfacher Ansatz, einen Hyperlink dynamisch zur Form Microsoft Visio hinzuzufügen.

Auf mehrseitigen Visio-Zeichnungen können Hyperlinks Sie von einer Seite zur anderen führen. Sie können Ihre Zeichnung auch mit einer Webseite oder einer Datei auf Ihrem System verknüpfen.

Diese Eigenschaften werden durch die ausgesetzt[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) Klasse unterstützt die[com.aspose.diagram.Hyperlink](https://reference.aspose.com/diagram/java/com.aspose.diagram/hyperlink) Objekt. Die add-Methode kann verwendet werden, um die Hyperlink-Daten einer Form hinzuzufügen.

Um Eigenschaften in Microsoft Visio zu identifizieren:

1. Klicken Sie in einem diagram mit der rechten Maustaste auf eine Form.
1.  Auswählen**Hyperlinks**.
1. Legen Sie vorhandene Eigenschaften fest
1.  Drücken Sie**OK** Taste

**Die Hyperlinkdaten einer Form, wie in Microsoft Visio zu sehen**

![todo: Bild_alt_Text](working-with-hyperlinks_1.png)

Die folgenden Codeausschnitte fügen die Hyperlinkdaten der Form hinzu.
### **Hyperlink-Programmierbeispiel hinzufügen**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddHyperlinkToShape.class);   
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(2);

//initialize Hyperlink object
Hyperlink hyperlink = new Hyperlink();
//set address value
hyperlink.getAddress().setValue("http://www.google.com/");
//set sub address value
hyperlink.getSubAddress().setValue("Sub address here");
//set description value
hyperlink.getDescription().setValue("Description here");
//set name
hyperlink.setName("MyHyperLink");

//add hyperlink to the shape
shape.getHyperlinks().add(hyperlink);            
//save diagram to local space
diagram.save(dataDir + "AddHyperlinkToShape_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Holen Sie sich Hyperlink-Daten der Visio-Shapes**
 Es ist möglich, die Hyperlink-Daten einer Form auf ähnliche Weise wie Sie abzurufen[Lesen von Visio Formdaten]().

Entwickler können alle Hyperlinks aus einem Visio-Shape auf die gleiche Weise abrufen wie sie[Visio Formdaten lesen]() verwenden[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/)

In mehrseitigen Visio-Zeichnungen können Sie durch Hyperlinks von einer Seite zur anderen gelangen. Sie können Ihre Zeichnung auch mit einer Webseite oder einer Datei auf Ihrem System verknüpfen.

Diese Eigenschaften werden durch die ausgesetzt[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) Klasse unterstützt die[com.aspose.diagram.Hyperlink](https://reference.aspose.com/diagram/java/com.aspose.diagram/hyperlink)Objekt. Die Eigenschaft kann verwendet werden, um die Hyperlinkdaten eines Shapes zu lesen.

Um Eigenschaften in Microsoft Visio zu identifizieren:

1. Klicken Sie in einem diagram mit der rechten Maustaste auf eine Form.
1.  Auswählen**Hyperlinks.**
 Alle vorhandenen Eigenschaften werden im Dialogfeld aufgelistet.

**Die Hyperlinkdaten einer Form, wie in Microsoft Visio zu sehen**

![todo: Bild_alt_Text](working-with-hyperlinks_2.png)

**Ein Konsolenfenster, das die Shape-Datenausgabe anzeigt**

![todo: Bild_alt_Text](working-with-hyperlinks_3.png)

Die folgenden Code-Snippets lesen die Hyperlink-Daten der Form.
### **Holen Sie sich das Hyperlinks-Programmierbeispiel**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetHyperlinks.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(1);
// iterate through the hyperlinks
for (Hyperlink hyperlink :(Iterable<Hyperlink>) shape.getHyperlinks())
{
    System.out.println("Address: " + hyperlink.getAddress().getValue());
    System.out.println("Sub Address: " + hyperlink.getSubAddress().getValue());
    System.out.println("Description: " + hyperlink.getDescription().getValue());
}

{{< /highlight >}}

