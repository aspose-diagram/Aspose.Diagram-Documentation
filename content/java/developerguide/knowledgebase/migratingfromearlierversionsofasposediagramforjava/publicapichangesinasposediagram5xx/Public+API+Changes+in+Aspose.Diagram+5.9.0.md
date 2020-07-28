+++
title = "Public API Changes in Aspose.Diagram 5.9.0" 
description = "" 
weight = 20080 
+++

Aspose.Diagram for Java : Public API Changes in Aspose.Diagram 5.9.0  

# Aspose.Diagram for Java : Public API Changes in Aspose.Diagram 5.9.0


This document describes changes to the Aspose.Diagram API from version 5.8.0 to 5.9.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behaviour behind the scenes in Aspose.Diagram. 

### Save Resultant HTML to a Stream 

The new save method has been added in the Diagram class. It takes two parameters, the stream object and the saving file format.  
Example code:

**Java**

{{< code lang="java" >}}
// Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram("Basic Flowchart.vsd");

// save resultant HTML directly to a stream
ByteArrayOutputStream dstStream = new ByteArrayOutputStream();
diagram.save(dstStream, SaveFileFormat.HTML);
// In you want to read the result into a Diagram object again, in Java you need to get the
// data bytes and wrap into an input stream.
ByteArrayInputStream srcStream = new ByteArrayInputStream(dstStream.toByteArray());
{{< /code >}}

### Copy Themes and PageSheet from Another Visio 

Diagram class offers CopyTheme method and PageSheet class offers Copy method to accomplish the goal of copying a shape and other manipulation tasks.  
Example codes: [Copy Shapes from an Existing Visio](http://www.aspose.com/docs/display/diagramjava/Copy+Shapes+from+an+Existing+Visio)

### VSTX and VSSX Saving Options are added in the SaveFileFormat

Previously, Aspose.Diagram API had supported reading and writing VSDX format, but now we have added support of writing diagrams in the VSTX and VSSX formats too. Example codes:

**Java**

{{< code lang="java" >}}
// save diagram in the VSTX format
diagram.save("C:\\temp\\Output.vstx", SaveFileFormat.VSTX);
// save diagram in the VSSX format
diagram.save("C:\\temp\\Output.vssx", SaveFileFormat.VSSX);
{{< /code >}}

### VSSX Reading Option is added in the LoadFileFormat

Previously, Aspose.Diagram API had supported reading and writing VSDX format, but now we have added support of reading VSSX stencil format too. Example codes:

**Java**

{{< code lang="java" >}}
// read VSSX stencil
Diagram diagram = new Diagram("C:\\temp\\Stencil.vssx", LoadFileFormat.VSSX);
{{< /code >}}

