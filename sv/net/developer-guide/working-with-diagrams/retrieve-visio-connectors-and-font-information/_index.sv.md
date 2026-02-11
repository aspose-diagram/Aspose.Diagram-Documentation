---
title: Hämta Visio Anslutningar och teckensnittsinformation
type: docs
weight: 20
url: /sv/net/retrieve-visio-connectors-and-font-information/
description: Det här avsnittet förklarar hur du får visio-kontakter och teckensnittsinformation.
---
## **Hämtar anslutningsinformation**
 Aspose.Diagram for .NET tillhandahåller mekanismer för att hämta information - ID och namn - om[sidor](/diagram/sv/net/retrieve-2c-get-2c-copy-and-insert-a-page/) och[bemästra](https://docs.aspose.com/diagram/net/working-with-masters/). Det låter dig också få information om kontakter, de element som länkar former.

 De[Ansluta](http://www.aspose.com/api/net/diagram/aspose.diagram/connect) objektet representerar en koppling som förenar två former på en Visio ritsida. Connects-egendomen, exponerad av[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page) klass stöder en samling av Aspose.Diagram. Connect-objekt. Den här egenskapen kan användas för att hämta ID- och namninformation om en koppling.
### **Programmeringsexempel**
Följande kodbit hämtar informationen för kontakterna i en diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "RetrieveConnectorInfo.vsd");

foreach (Aspose.Diagram.Connect connector in vdxDiagram.Pages[0].Connects)
{
    // Display information about the Connectors
    Console.WriteLine("\nFrom Shape ID : " + connector.FromSheet);
    Console.WriteLine("To Shape ID : " + connector.ToSheet);
}

{{< /highlight >}}
```
## **Hämtar teckensnittsinformation**
 Aspose.Diagram har mekanismer för att hämta information om de element som utgör en diagram, från[sidor](/diagram/sv/net/retrieve-2c-get-2c-copy-and-insert-a-page/), [stenciler](https://docs.aspose.com/diagram/net/working-with-masters/), [kontakter](/diagram/sv/net/retrieving-connector-information/)och även typsnitt. Den här artikeln visar hur du tar reda på vilka teckensnitt som används i en diagram.

 De[Font](http://www.aspose.com/api/net/diagram/aspose.diagram/font) objekt representerar ett typsnitt som antingen appliceras på text i ett dokument eller tillgängligt för användning i systemet. Ett teckensnittsobjekt mappar ett namn (till exempel "Arial") till teckensnitts-ID (till exempel 3) som Microsoft Visio lagrar i en typsnittscell i ett teckenavsnitt i en form som innehåller text formaterad med det teckensnittet. Teckensnitts-ID kan ändras när ett dokument öppnas på olika system eller när teckensnitt installeras eller tas bort.
### **Hämtar teckensnittsprogrammeringsexempel**
Följande kodbit hämtar teckensnittsinformation från Visio diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "RetrieveFontInfo.vsd");

foreach (Aspose.Diagram.Font font in vdxDiagram.Fonts)
{
    // Display information about the fonts
    Console.WriteLine(font.Name);
}

{{< /highlight >}}
```
### **Hämta standardfontkatalog**
Aspose.Diagram for .NET API gör det också möjligt att hämta standardsökväg för teckensnittskatalog med metoden GetDefaultFontDir() i klassen Diagram. Följande kodbit hämtar standardteckensnittskatalogen från Visio diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "RetrieveFontInfo.vsd");
           
// Display font default directory
Console.WriteLine(vdxDiagram.GetDefaultFontDir());

{{< /highlight >}}
```
### **Få oanvända teckensnitt**
{{% alert color="primary" %}}

Denna metod stöds av version 19.6 eller senare.

{{% /alert %}}

Aspose.Diagram for .NET API tillåter också att få oanvända teckensnitt med metoden GetUnusedStyles() i klassen Diagram. Följande kodbit hämtar oanvända teckensnitt från Visio diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Call the diagram constructor to load diagram from a VSD file
Diagram vdxDiagram = new Diagram(dataDir + "Sample_UnusedFonts.vsdx");

// Get Unused Fonts 
StyleSheetCollection unused = vdxDiagram.GetUnusedStyles();

// Display unused fonts count 
Console.WriteLine(unused.Count);

{{< /highlight >}}
```
