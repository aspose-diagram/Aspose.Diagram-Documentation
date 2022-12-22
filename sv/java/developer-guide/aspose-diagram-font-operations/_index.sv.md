---
title: Aspose.Diagram Font Operations
type: docs
weight: 170
url: /sv/java/aspose-diagram-font-operations/
---
{{% alert color="primary" %}} 

Aspose.Diagram låter utvecklare ställa in teckensnittskatalogerna för rendering i Visio-diagram. Den här artikeln visar hur du använder teckensnitt från anpassade kataloger.

{{% /alert %}} 
### **Arbeta med teckensnitt**
#### **Där Aspose.Diagram letar efter TrueType-teckensnitt på Windows**
 Aspose.Diagram söker efter teckensnitt i**Windows\Teckensnitt** mapp. Den här standardinställningen fungerar för det mesta så ange bara dina egna teckensnittsmappar om du verkligen behöver det.
#### **Hur man explicit anger en typsnittsmapp**
 Aspose.Diagram API:er har exponerat setFontDirs-metoden för[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) klass för att ange typsnittsmapparna enligt beskrivningen nedan.

1. Metoden Diagram.setFontDirs tar en strängarray som parameter, så utvecklaren kan ange många teckensnittskataloger med detta tillvägagångssätt.

{{% alert color="primary" %}} 

När du anger teckensnittsmappen med ovan nämnda tillvägagångssätt rekommenderar vi att du ställer in teckensnittsplatsen i början av programmet, annars kan du få dåligt formaterade resultat.

{{% /alert %}} {{% alert color="primary" %}} 

Att ställa in teckensnittsmappen med någon av ovanstående metoder säkerställer inte att Aspose.Diagram API inte letar efter teckensnitten på standardplatser som systemets teckensnittsmapp.

{{% /alert %}} 

Demonstrerar hur du ställer in Aspose.Diagram att leta efter TrueType-teckensnitt i flera mappar när du renderar eller bäddar in teckensnitt.
#### **Programmeringsexempel**
Kodexemplet nedan visar hur du ställer in Aspose.Diagram att leta efter TrueType-teckensnitt i flera mappar när du renderar eller bäddar in teckensnitt.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Fonts-SpecifyFontLocation-SpecifyFontLocation.java" >}}
### **Ta emot meddelande om saknade teckensnitt och teckensnittsersättning under rendering**
Aspose.Diagram API kräver åtkomst till det korrekta teckensnittet för att ritningen ska kunna återges korrekt i formatet PDF. Om det önskade teckensnittet inte är tillgängligt på maskinen, renderar Aspose.Diagram API någon instans av det teckensnittet med standardteckensnittet eller det närmaste tillgängliga teckensnittet på maskinen, eftersom denna ersättning kan ändra utseendet på den renderade ritningen, kan utvecklare behöva meddelas när ett typsnitt saknas och med vilket typsnitt det kommer att ersättas med.
#### **Meddelande om saknade teckensnitt och teckensnittsersättningsprogrammeringsexempel**
För att meddelas om teckensnittsersättning under rendering:

1. Skapa en klass som implementerar[IWarningCallback](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)
1. Skicka den till egenskapen PdfSaveOptions.setWarningCallback(com.aspose.diagram.IWarningCallback).

Under sparandet av ritningen instansen av[IWarningCallback](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)anropas om det finns några potentiella trohetsproblem med ritningen. I det här fallet väljer vi att endast behandla varningar som är för teckensnittsersättning och skriva ut varningen på skärmen. Exemplet nedan visar hur du får meddelanden om teckensnittsersättningar genom att använda[IWarningCallback](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback).

**Java**

{{< highlight "java" >}}

 // load the document to render.

Diagram diagram = new Diagram("C:\\temp\\Output.vsdx");


// initialize PdfSaveOptions object

com.aspose.diagram.PdfSaveOptions saveOp = new com.aspose.diagram.PdfSaveOptions();

// create a new class implementing IWarningCallback which collect any warnings produced during drawing save.

HandleDocumentWarnings callback = new HandleDocumentWarnings();

saveOp.setWarningCallback(callback);



// pass the save options along with the save path to the save method.

diagram.save("C:\\temp\\Rendering.MissingFontNotification Out.pdf", saveOp);

{{< /highlight >}}
#### **Implementering av IWarningCallback**
Det sista steget är att skapa klassen som implementerar[IWarningCallback](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)gränssnitt. Denna klass kommer att skriva ut alla varningar om teckensnittsersättning till konsolen. Exemplet nedan visar hur man implementerar IWarningCallback för att bli meddelad om teckensnittsersättning under dokumentspara.



**Java**

{{< highlight "java" >}}

 public class HandleDocumentWarnings implements IWarningCallback {

     /**

     * Our callback only needs to implement the "Warning" method. This method is

     * called whenever there is a potential issue during document processing.

     * The callback can be set to listen for warnings generated during document

     * load and/or document save.

     */

     public void warning(WarningInfo info) {

         // We are only interested in fonts being substituted.

         if (info.getWarningType() == WarningType.FONT_SUBSTITUTION) {

         System.out.println("Font substitution: " + info.getDescription());

     }

 }

}

{{< /highlight >}}
