---
title: Aspose.Diagram Font Operations
type: docs
weight: 180
url: /sv/net/aspose-diagram-font-operations/
description: Den här sidan beskriver hur man manipulerar teckensnitt med Aspose.Diagram-biblioteket.
---
## **Så här anger du TrueType-teckensnittsplats**
Aspose.Diagram låter utvecklare ställa in teckensnittskatalogerna för rendering i Visio-diagram. Den här artikeln visar hur du använder teckensnitt från anpassade kataloger.
### **Arbeta med teckensnitt**
#### **Där Aspose.Diagram letar efter TrueType-teckensnitt på Windows**
 Aspose.Diagram söker efter teckensnitt i**Windows\Teckensnitt** mapp. Den här standardinställningen fungerar för det mesta så ange bara dina egna teckensnittsmappar om du verkligen behöver det.
#### **Hur man explicit anger en typsnittsmapp**
Aspose.Diagram API:er har exponerat FontDirs-egenskapen för[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) klass för att ange typsnittsmapparna enligt beskrivningen nedan.

1. Egenskapen Diagram.FontDirs accepterar en strängmatris så utvecklaren kan ange många teckensnittskataloger med detta tillvägagångssätt.

{{% alert color="primary" %}} 

När du anger teckensnittsmappen med ovan nämnda tillvägagångssätt rekommenderar vi att du ställer in teckensnittsplatsen i början av programmet, annars kan du få dåligt formaterade resultat.

{{% /alert %}} {{% alert color="primary" %}} 

Att ställa in teckensnittsmappen med någon av ovanstående metoder säkerställer inte att Aspose.Diagram API inte letar efter teckensnitten på standardplatser som systemets teckensnittsmapp.

{{% /alert %}} 
#### **Programmeringsexempel**
Kodexemplet nedan visar hur du ställer in Aspose.Diagram att leta efter TrueType-teckensnitt i flera mappar när du renderar eller bäddar in teckensnitt.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

String[] fontDirs = new String[] { "C:\\MyFonts\\", "D:\\Misc\\Fonts\\" };
// Load the Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Setting the custom font directories
diagram.FontDirs = fontDirs;

// Saving Visio diagram in PDF format
diagram.Save(dataDir + "SpecifyFontLocation_out.pdf", SaveFileFormat.PDF);

{{< /highlight >}}
```
### **Ta emot meddelande om saknade teckensnitt och teckensnittsersättning under rendering**
Aspose.Diagram API kräver åtkomst till det korrekta teckensnittet för att ritningen ska kunna återges korrekt i formatet PDF. Om det önskade teckensnittet inte är tillgängligt på maskinen, renderar Aspose.Diagram API någon instans av det teckensnittet med standardteckensnittet eller det närmaste tillgängliga teckensnittet på maskinen, eftersom denna ersättning kan ändra utseendet på den renderade ritningen, kan utvecklare behöva meddelas när ett typsnitt saknas och med vilket typsnitt det kommer att ersättas med.
#### **Meddelande om saknade teckensnitt och teckensnittsersättningsprogrammeringsexempel**
För att meddelas om teckensnittsersättning under rendering:

1. Skapa en klass som implementerar[IWarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback)
1. Skicka den till egenskapen PdfSaveOptions.WarningCallback.

Under sparandet av ritningen instansen av[IWarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback)anropas om det finns några potentiella trohetsproblem med ritningen. I det här fallet väljer vi att endast behandla varningar som är för teckensnittsersättning och skriva ut varningen på skärmen. Exemplet nedan visar hur du får meddelanden om teckensnittsersättningar genom att använda[IWarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback).

**C#**

{{< highlight "java" >}}

 // The path to the documents directory.

string dataDir = RunExamples.GetDataDir_Intro();

// load the document to render.

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// initialize PdfSaveOptions object

PdfSaveOptions saveOp = new PdfSaveOptions();

// create a new class implementing IWarningCallback which collect any warnings produced during drawing save.

HandleDocumentWarnings callback = new HandleDocumentWarnings();

saveOp.WarningCallback = callback;

// pass the save options along with the save path to the save method.

diagram.Save(dataDir + "NotificationofMissingFonts_Out.pdf", saveOp);

{{< /highlight >}}
#### **Implementering av IWarningCallback**
Det sista steget är att skapa klassen som implementerar[IWarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram/IWarningCallback)gränssnitt. Denna klass kommer att skriva ut alla varningar om teckensnittsersättning till konsolen. Exemplet nedan visar hur man implementerar IWarningCallback för att bli meddelad om teckensnittsersättning under dokumentspara.

**C#**

{{< highlight "java" >}}

 class HandleDocumentWarnings : IWarningCallback

{

    /**

    * Our callback only needs to implement the "Warning" method. This method is

    * called whenever there is a potential issue during document processing.

    * The callback can be set to listen for warnings generated during document

    * load and/or document save.

    */

    public void Warning(WarningInfo info)

    {

        // We are only interested in fonts being substituted.

        if (info.WarningType == WarningType.FontSubstitution)

        {

            Console.WriteLine("Font substitution: " + info.Description);

        }

    }

}

{{< /highlight >}}
