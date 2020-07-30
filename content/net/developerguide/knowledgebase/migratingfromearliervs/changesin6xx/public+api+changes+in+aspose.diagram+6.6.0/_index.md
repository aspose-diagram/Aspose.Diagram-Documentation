---
title : "Public API Changes in Aspose.Diagram 6.6.0" 
description : "" 
weight : 20074 
toc : false
type: docs
url: /net/developerguide/knowledgebase/migratingfromearliervs/changesin6xx/public+api+changes+in+aspose.diagram+6.6.0/
---

# Aspose.Diagram for .NET : Public API Changes in Aspose.Diagram 6.6.0


This document describes changes to the Aspose.Diagram API from version 6.3.0 to 6.6.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.Diagram.

### Adds VSDM, VSSM and VSTM formats in LoadFileFormat class

This version adds support of reading macro-enabled Visio formats.

### Adds VSDM, VSSM and VSTM formats in SaveFileFormat class

This version adds support of writing macro-enabled Visio formats.

### Modify VBA Module Code in the Visio Diagram

We have added VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference and VbaProjectReferenceCollection classes. These classes help to get control over VBA project. Using this new version 6.6.0 or higher, developers can extract and modify VBA module code. Please check this code example:

**C#**

{{< code lang="c#" >}}
// load an existing Visio diagram
Diagram diagram = new Diagram(@"c:\temp\macro.vsdm", LoadFileFormat.VSDM);
// extract VBA project
Aspose.Diagram.Vba.VbaProject v = diagram.VbaProject;
// Iterate through the modules and modify VBA module code
foreach (VbaModule module in diagram.VbaProject.Modules)
{
    string code = module.Codes;
    if (code.Contains("This is test message."))
        code = code.Replace("This is test message.", "This is Aspose.Diagram message.");
    module.Codes = code;
}
// save the Visio diagram
diagram.Save(@"c:\temp\out.vssm", SaveFileFormat.VSSM);
{{< /code >}}

Error rendering macro 'code' : Invalid value specified for parameter lang

### Adds an ImageData property in ForeignData class

It represents an image of ole object as a byte array. Besides this, we have also enhanced the manipulation of OLE objects. Developers can now also replace an OLE object in the Visio diagram. Please check this code example:

**C#**

{{< code lang="c#" >}}
// load a Visio diagram
Diagram diagram = new Diagram(DirPath + "Drawing1.vsdx");
// get page of the Visio diagram by name
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");
// get shape of the Visio diagram by ID
Aspose.Diagram.Shape OLE_Shape = page.Shapes.GetShape(2);

// filter shapes by type Foreign
if (OLE_Shape.Type == Aspose.Diagram.TypeValue.Foreign)
{
    if (OLE_Shape.ForeignData.ForeignType == ForeignType.Object)
    {
        Stream Ole_stream = new MemoryStream(OLE_Shape.ForeignData.ObjectData);
        // get format of the OLE file object
        Aspose.Words.FileFormatInfo info = Aspose.Words.FileFormatUtil.DetectFileFormat(Ole_stream);
        if (info.LoadFormat == Aspose.Words.LoadFormat.Doc || info.LoadFormat == Aspose.Words.LoadFormat.Docx)
        {
            // modify an OLE object
            var doc = new Aspose.Words.Document(new MemoryStream(OLE_Shape.ForeignData.ObjectData));
            doc.Range.Replace("testing", "Aspose", false, true);
            MemoryStream outStream = new MemoryStream();
            doc.Save(outStream, Aspose.Words.SaveFormat.Docx);
            // save back an OLE object
            OLE_Shape.ForeignData.ObjectData = outStream.ToArray();
        }
    }
}
// save Visio diagram
diagram.Save(DirPath + "modified.vsdx", SaveFileFormat.VSDX);
{{< /code >}}

Error rendering macro 'code' : Invalid value specified for parameter lang

