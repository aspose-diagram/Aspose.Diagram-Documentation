---
title: Manipuler les objets OLE intégrés dans Visio Diagram
type: docs
weight: 10
url: /fr/net/manipulate-the-embedded-ole-objects-in-visio-diagram/
description: Cette page décrit comment manipuler l'objet ole avec la bibliothèque Aspose.Diagram.
---
{{% alert color="primary" %}}

Microsoft Office Visio prend en charge la manipulation des objets OLE dans le Visio diagram. Si un fichier visio réside en dehors du dessin Visio et que les développeurs doivent ajouter une fonctionnalité dans leurs applications .NET pour insérer automatiquement ces fichiers dans le dessin, ils peuvent y parvenir en utilisant[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

{{% /alert %}}
## **Manipuler l'exemple de programmation d'objets OLE intégrés**
[ObjectData](http://www.aspose.com/api/net/diagram/aspose.diagram/foreigndata/properties/objectdata) propriété de la[Données étrangères](http://www.aspose.com/api/net/diagram/aspose.diagram/foreigndata)permet aux développeurs de manipuler avec des objets OLE existants dans Visio diagram. Cette rubrique d'aide montre comment les développeurs peuvent récupérer un objet OLE du document Word, le modifier à l'aide[Aspose.Words for .NET API](https://products.aspose.com/words/net), puis enregistrez-le en tant qu'objet OLE dans le fichier Visio diagram.

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
