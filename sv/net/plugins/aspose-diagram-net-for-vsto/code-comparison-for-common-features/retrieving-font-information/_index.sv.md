---
title: Hämtar teckensnittsinformation
type: docs
weight: 80
url: /sv/net/retrieving-font-information/
---
## **VSTO**
Nedan finns koden för att hämta teckensnittsinformation:

{{< highlight "cs" >}}

  foreach (Font font in Application.ActiveDocument.Fonts)

 {

    //Display information about the fonts

    MessageBox.Show(font.Name);

 }

{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

 Aspose.Diagram har mekanismer för att hämta information om de element som utgör en diagram, från[sidor](https://reference.aspose.com/diagram/net/aspose.diagram/pagecollection) , schabloner,[kontakter](/diagram/sv/net/retrieving-connector-information/)och även typsnitt. Den här artikeln visar hur du tar reda på vilka teckensnitt som används i en diagram.

{{% /alert %}} 

 De[Font](https://reference.aspose.com/diagram/net/aspose.diagram/font) objekt representerar ett typsnitt som antingen appliceras på text i ett dokument eller tillgängligt för användning i systemet.

Ett teckensnittsobjekt mappar ett namn (till exempel "Arial") till teckensnitts-ID (till exempel 3) som Microsoft Visio lagrar i en typsnittscell i ett teckenavsnitt i en form som innehåller text formaterad med det teckensnittet. Teckensnitts-ID kan ändras när ett dokument öppnas på olika system eller när teckensnitt installeras eller tas bort.

{{< highlight "cs" >}}

  //Call the diagram constructor to load diagram from a VDX file

 Diagram vdxDiagram = new Diagram(@"E:\Aspose\Aspose Vs VSTO\Aspose.Diagram Vs VSTO Visio v1.1\Sample Files\Drawing1.vdx");

 foreach (Aspose.Diagram.Font font in vdxDiagram.Fonts)

 {

    //Display information about the fonts

    Console.WriteLine(font.Name);

 }

{{< /highlight >}}
## **Ladda ner exempelkod**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Ladda ner Running Code**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Retrieving%20Font%20Information)
