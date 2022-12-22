---
title: Skriva dokumentsammanfattning
type: docs
weight: 70
url: /sv/net/writing-document-summary/
---
## **VSTO**
Nedan är koden för att skriva dokumentsammanfattning av Visio:

{{< highlight "cs" >}}

  Application.ActiveDocument.Creator = "Zeeshan";

 Application.ActiveDocument.Company = "Aspose";

 Application.ActiveDocument.Category = "Drawing 2D";

 Application.ActiveDocument.Manager = "Self";

 Application.ActiveDocument.Title = "Zeeshan";

 Application.ActiveDocument.Subject = "Visio Diagram";


{{< /highlight >}}
## **Aspose.Diagram**
{{% alert color="primary" %}} 

Microsoft Visio låter dig definiera ett antal egenskaper för dokumentsammanfattningsinformation för att hjälpa dig och dina kollegor att identifiera en diagram. Sammanfattningsegenskaper, till exempel titel, ämne, författare och beskrivning, gör filen lättare att hitta när du söker och lättare att känna igen när du surfar filer.

{{% /alert %}} 
### **Skriver Microsoft Visio Dokumentsammanfattning Info**
 De[Dokument egenskaper](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties)klass exponerar ett antal egenskaper för att ställa in eller få en Microsoft Visio diagram sammanfattande information. Aspose.Diagram for .NET kan uppdatera ritningssammanfattningsinformationen och sedan skriva tillbaka ritningsfilen till VDX.

Så här uppdaterar du ritningssammanfattningsinformationen för en befintlig VDX- eller VSD-fil:

1.  Skapa en instans av[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram) klass.
1. Ställ in egenskaper som exponeras av Diagram.DocumentProps för att definiera sammanfattningsinformationen för ritningsfilen Visio.
1. Ring Diagram-klassens Spara-metod för att skriva Visio-ritningsfilen till VDX.

Kontrollera sammanfattningsinformationen:

1. Öppna utdatafilen VDX i Microsoft Visio.
1.  Väljer**Info** från**Fil** meny.

{{< highlight "cs" >}}

  //Call the diagram constructor to load diagram from a VDX file

 Diagram vdxDiagram = new Diagram("Drawing1.vdx");

 //Set some summary information about the diagram

 vdxDiagram.DocumentProps.Creator = "Ijaz";

 vdxDiagram.DocumentProps.Company = "Aspose";

 vdxDiagram.DocumentProps.Category = "Drawing 2D";

 vdxDiagram.DocumentProps.Manager = "Sergey Polshkov";

 vdxDiagram.DocumentProps.Title = "Aspose Title";

 vdxDiagram.DocumentProps.TimeCreated = DateTime.Now;

 vdxDiagram.DocumentProps.Subject = "Visio Diagram";

 vdxDiagram.DocumentProps.Template = "Aspose Template";

 //Write the updated file to the disk in VDX file format

 vdxDiagram.Save("output.vdx", SaveFileFormat.VDX);


{{< /highlight >}}
## **Ladda ner exempelkod**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Ladda ner Running Code**
- [Github](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Writing%20Document%20Summary)
