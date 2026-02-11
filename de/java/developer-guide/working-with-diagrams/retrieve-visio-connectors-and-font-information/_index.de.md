---
title: Rufen Sie Visio-Konnektoren und Schriftartinformationen ab
type: docs
weight: 20
url: /de/java/retrieve-visio-connectors-and-font-information/
---
## **Abrufen von Connector-Informationen**
 Aspose.Diagram for Java bietet Mechanismen zum Abrufen von Informationen – ID und Name – über[Seiten](/diagram/de/java/retrieve-get-copy-and-insert-a-page/) und[Meister](). Außerdem erhalten Sie Informationen zu Verbindungselementen, den Elementen, die Formen verbinden.

 Das[Verbinden](https://reference.aspose.com/diagram/java/com.aspose.diagram/connect) -Objekt stellt einen Verbinder dar, der zwei Shapes auf einem Zeichenblatt Visio verbindet. Die Connects-Eigenschaft, verfügbar gemacht durch die[Buchseite](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) -Klasse unterstützt eine Sammlung von Aspose.Diagram.Connect-Objekten. Diese Eigenschaft kann verwendet werden, um ID- und Namensinformationen zu einem Connector abzurufen.

**Ein Konsolenfenster, das die Ausgabe des folgenden Codes zeigt.** 

![todo: Bild_alt_Text](retrieve-visio-connectors-and-font-information_1.png)
### **Programmierbeispiel**
Der folgende Codeabschnitt ruft die Informationen für die Connectors in einem diagram ab.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveConnectorInfo.class);
        
//Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "RetrieveConnectorInfo.vsd");        
for(Connect connector : (Iterable<Connect>) diagram.getPages().getPage(0).getConnects())
{
    // Display information about the Connectors
    System.out.println("\nFrom Shape ID : " + connector.getFromSheet());
    System.out.println("To Shape ID : " + connector.getToSheet());
 }

System.out.println("Process Completed Successfully");

{{< /highlight >}}

## **Abrufen von Schriftinformationen**
 Aspose.Diagram verfügt über Mechanismen zum Abrufen von Informationen über die Elemente, aus denen diagram besteht[Seiten](/diagram/de/java/retrieve-get-copy-and-insert-a-page/), [Schablonen](), [Anschlüsse](https://reference.aspose.com/diagram/java/com.aspose.diagram/ConnectCollection)und auch Schriftarten. Dieser Artikel zeigt, wie Sie herausfinden, welche Schriftarten in einer diagram verwendet werden.

 Das[Schriftart](https://reference.aspose.com/diagram/java/com.aspose.diagram/font) Objekt stellt eine Schriftart dar, die entweder auf Text in einem Dokument angewendet wird oder zur Verwendung auf dem System verfügbar ist.

Ein Font-Objekt ordnet einen Namen (z. B. „Arial“) der Schriftart-ID (z. B. 3) zu, die Microsoft Visio in einer Font-Zelle in einem Zeichenabschnitt einer Form speichert, die mit dieser Schriftart formatierten Text enthält. Schriftart-IDs können sich ändern, wenn ein Dokument auf verschiedenen Systemen geöffnet wird oder wenn Schriftarten installiert oder entfernt werden.
### **Abrufen des Font-Programmierbeispiels**
Der folgende Codeabschnitt ruft Schriftartinformationen von Visio diagram ab.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrieveFontInfo.class);

// call the diagram constructor to load diagram
Diagram diagram = new Diagram(dataDir+ "RetrieveFontInfo.vsd");

for(Font font : (Iterable<Font>) diagram.getFonts())
{
    // Display information about the fonts
    System.out.println(font.getName());
}

System.out.println("Process Completed Successfully");

{{< /highlight >}}


![todo: Bild_alt_Text](retrieve-visio-connectors-and-font-information_2.png)
### **Abrufen des Standardschriftverzeichnisses**
Aspose.Diagram for Java API ermöglicht auch das Abrufen des Standardverzeichnispfads für Schriftarten mithilfe der Methode getDefaultFontDir() der Klasse Diagram. Der folgende Codeabschnitt ruft das Standardverzeichnis für Schriftarten aus dem Verzeichnis Visio diagram ab.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveFontInfo.class) + "Diagrams/";

// Call the diagram constructor to load diagram
Diagram diagram = new Diagram(dataDir + "RetrieveFontInfo.vsd");

// Display font default directory
System.out.println(diagram.getDefaultFontDir());

{{< /highlight >}}

