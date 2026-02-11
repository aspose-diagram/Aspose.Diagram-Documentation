---
title: Manipular los objetos OLE incrustados en Visio Diagram
type: docs
weight: 10
url: /es/net/manipulate-the-embedded-ole-objects-in-visio-diagram/
description: Esta página describe cómo manipular un objeto ole con la biblioteca Aspose.Diagram.
---
{{% alert color="primary" %}}

Microsoft Office Visio admite la manipulación de objetos OLE en Visio diagram. Si un archivo visio reside fuera del dibujo Visio y los desarrolladores necesitan agregar una característica en sus aplicaciones .NET para insertar automáticamente estos archivos dentro del dibujo, pueden lograrlo usando[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

{{% /alert %}}
## **Manipular el ejemplo de programación de objetos OLE incrustados**
[ObjetoDatos](http://www.aspose.com/api/net/diagram/aspose.diagram/foreigndata/properties/objectdata) propiedad de la[ForeignData](http://www.aspose.com/api/net/diagram/aspose.diagram/foreigndata)class permite a los desarrolladores manipular con objetos OLE existentes en Visio diagram. Este tema de ayuda demuestra cómo los desarrolladores pueden recuperar un objeto OLE del documento de Word, editarlo usando[Aspose.Words for .NET API](https://products.aspose.com/words/net)y luego guárdelo como un objeto OLE en el Visio diagram.

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
