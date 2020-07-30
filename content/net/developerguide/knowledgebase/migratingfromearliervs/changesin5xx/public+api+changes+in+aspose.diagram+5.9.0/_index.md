---
title : "Public API Changes in Aspose.Diagram 5.9.0" 
description : "" 
weight : 20078 
toc : false
type: docs
url: /net/developerguide/knowledgebase/migratingfromearliervs/changesin5xx/public+api+changes+in+aspose.diagram+5.9.0/
---

# Aspose.Diagram for .NET : Public API Changes in Aspose.Diagram 5.9.0


This document describes changes to the Aspose.Diagram API from version 5.8.0 to 5.9.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.Diagram.

### Save Resultant HTML to a Stream 

The new Save method has been added in the Diagram class. It takes two parameters, the stream object and the saving file format.  
Example code:

**C#**

{{< code lang="c#" >}}
// load an existing visio diagram
Diagram diagram = new Diagram("Basic Flowchart.vsd");

// save resultant HTML directly to a stream
MemoryStream stream = new MemoryStream();
diagram.Save(stream, SaveFileFormat.HTML);
{{< /code >}}

**VB**

{{< code lang="vb" >}}
' load an existing visio diagram
Dim diagram As Diagram = New Diagram("Basic Flowchart.vsd")

' save resultant HTML directly to a stream
MemoryStream stream = new MemoryStream()
diagram.Save(stream, SaveFileFormat.HTML)
{{< /code >}}

### Copy Themes and PageSheet from Another Visio 

Diagram class offers CopyTheme method and PageSheet class offers Copy method to accomplish the goal of copying a shape and other manipulation tasks.  
Example codes: [Copy Shapes from an Existing Visio](http://www.aspose.com/docs/display/diagramnet/Copy+Shapes+from+an+Existing+Visio)

### VSTX and VSSX Saving Options are added in the SaveFileFormat

Previously, Aspose.Diagram API had supported reading and writing VSDX format, but now we have added support of writing diagrams in the VSTX and VSSX formats too. Example codes:

**C#**

{{< code lang="c#" >}}
// save diagram in the VSTX format
diagram.Save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX);
// save diagram in the VSSX format
diagram.Save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX);
{{< /code >}}

**VB**

{{< code lang="vb" >}}
' save diagram in the VSTX format
diagram.Save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX)
' save diagram in the VSSX format
diagram.Save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX)
{{< /code >}}

### VSSX Reading Option is added in the LoadFileFormat

Previously, Aspose.Diagram API had supported reading and writing VSDX format, but now we have added support of reading VSSX stencil format too. Example codes:

**C#**

{{< code lang="c#" >}}
// read VSSX stencil
Diagram diagram = new Diagram(@"C:\temp\Stencil.vssx", LoadFileFormat.VSSX);
{{< /code >}}

**VB**

{{< code lang="vb" >}}
' read VSSX stencil
Diagram diagram = new Diagram(@"C:\temp\Stencil.vssx", LoadFileFormat.VSSX)
{{< /code >}}

