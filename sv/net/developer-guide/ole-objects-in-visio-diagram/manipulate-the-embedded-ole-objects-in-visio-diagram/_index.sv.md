---
title: Manipulera de inbäddade OLE-objekten i Visio Diagram
type: docs
weight: 10
url: /sv/net/manipulate-the-embedded-ole-objects-in-visio-diagram/
description: Den här sidan beskriver hur man manipulerar ett ole-objekt med Aspose.Diagram-biblioteket.
---
{{% alert color="primary" %}}

Microsoft Office Visio stöder manipulering av OLE-objekten i Visio diagram. Om en visio-fil finns utanför Visio-filerna behöver de lägga till en 17 i dessa applikationer i Visio-filerna, och utvecklarna kan lägga till en 17-funktion i denna applikation i Visio.[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

{{% /alert %}}
## **Manipulera programmeringsexemplet för inbäddade OLE-objekt**
[Objektdata](http://www.aspose.com/api/net/diagram/aspose.diagram/foreigndata/properties/objectdata) egendom av[ForeignData](http://www.aspose.com/api/net/diagram/aspose.diagram/foreigndata)klass tillåter utvecklare att manipulera med befintliga OLE-objekt i Visio diagram. Det här hjälpämnet visar hur utvecklare kan hämta ett OLE-objekt i Word-dokumentet, redigera det med hjälp av[Aspose.Words for .NET API](https://products.aspose.com/words/net), och spara sedan tillbaka som ett OLE-objekt i Visio diagram.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_OLEObjects();

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page of the Visio diagram by name
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");
// Get shape of the Visio diagram by ID
Aspose.Diagram.Shape OLE_Shape = page.Shapes.GetShape(2);

// Filter shapes by type Foreign
if (OLE_Shape.Type == Aspose.Diagram.TypeValue.Foreign)
{
    if (OLE_Shape.ForeignData.ForeignType == ForeignType.Object)
    {
        Stream Ole_stream = new MemoryStream(OLE_Shape.ForeignData.ObjectData);
        // Get format of the OLE file object
        Aspose.Words.FileFormatInfo info = Aspose.Words.FileFormatUtil.DetectFileFormat(Ole_stream);
        if (info.LoadFormat == Aspose.Words.LoadFormat.Doc || info.LoadFormat == Aspose.Words.LoadFormat.Docx)
        {
            // Modify an OLE object
            var doc = new Aspose.Words.Document(new MemoryStream(OLE_Shape.ForeignData.ObjectData));
            doc.Range.Replace("testing", "Aspose", false, true);
            MemoryStream outStream = new MemoryStream();
            doc.Save(outStream, Aspose.Words.SaveFormat.Docx);
            // Save back an OLE object
            OLE_Shape.ForeignData.ObjectData = outStream.ToArray();
        }
    }
}
// Save Visio diagram
diagram.Save(dataDir + "ManipulateObjects_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
