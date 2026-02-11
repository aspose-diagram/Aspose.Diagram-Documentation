---
title: Hämta Visio Anslutningar och teckensnittsinformation
type: docs
weight: 20
url: /sv/java/retrieve-visio-connectors-and-font-information/
---
## **Hämtar anslutningsinformation**
 Aspose.Diagram for Java tillhandahåller mekanismer för att hämta information - ID och namn - om[sidor](/diagram/sv/java/retrieve-get-copy-and-insert-a-page/) och[bemästra](). Det låter dig också få information om kontakter, de element som länkar former.

 De[Ansluta](https://reference.aspose.com/diagram/java/com.aspose.diagram/connect) objektet representerar en koppling som förenar två former på en Visio ritsida. Connects-egendomen, exponerad av[Sida](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) klass stöder en samling av Aspose.Diagram. Connect-objekt. Den här egenskapen kan användas för att hämta ID- och namninformation om en koppling.

**Ett konsolfönster som visar utdata från koden nedan.** 

![todo:image_alt_text](retrieve-visio-connectors-and-font-information_1.png)
### **Programmeringsexempel**
Följande kodbit hämtar informationen för kontakterna i en diagram.

```
{{< highlight "java" >}}
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
```
## **Hämtar teckensnittsinformation**
 Aspose.Diagram har mekanismer för att hämta information om de element som utgör en diagram, från[sidor](/diagram/sv/java/retrieve-get-copy-and-insert-a-page/), [stenciler](), [kontakter](https://reference.aspose.com/diagram/java/com.aspose.diagram/ConnectCollection)och även typsnitt. Den här artikeln visar hur du tar reda på vilka teckensnitt som används i en diagram.

 De[Font](https://reference.aspose.com/diagram/java/com.aspose.diagram/font) objekt representerar ett typsnitt som antingen appliceras på text i ett dokument eller tillgängligt för användning i systemet.

Ett teckensnittsobjekt mappar ett namn (till exempel "Arial") till teckensnitts-ID (till exempel 3) som Microsoft Visio lagrar i en typsnittscell i ett teckenavsnitt i en form som innehåller text formaterad med det teckensnittet. Teckensnitts-ID kan ändras när ett dokument öppnas på olika system eller när teckensnitt installeras eller tas bort.
### **Hämtar teckensnittsprogrammeringsexempel**
Följande kodbit hämtar teckensnittsinformation från Visio diagram.

```
{{< highlight "java" >}}
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
```

![todo:image_alt_text](retrieve-visio-connectors-and-font-information_2.png)
### **Hämta standardfontkatalog**
Aspose.Diagram for Java API gör det också möjligt att hämta standardsökväg för teckensnittskatalog med metoden getDefaultFontDir() i klassen Diagram. Följande kodbit hämtar standardteckensnittskatalogen från Visio diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveFontInfo.class) + "Diagrams/";

// Call the diagram constructor to load diagram
Diagram diagram = new Diagram(dataDir + "RetrieveFontInfo.vsd");

// Display font default directory
System.out.println(diagram.getDefaultFontDir());

{{< /highlight >}}
```
