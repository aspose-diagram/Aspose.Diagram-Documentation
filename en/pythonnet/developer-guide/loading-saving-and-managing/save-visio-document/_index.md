---
title: Save Visio document programmatically
linktitle: Save Visio document
type: docs
weight: 30
url: /python-net/save-visio-document/
description: This page describes how to save Visio document to file, stream with Aspose.Diagram library.
---

## **Visio Drawing Save Overview**
Use the [Diagram.Save]() method to save a Microsoft Visio drawing. There are overloads that allow saving a drawing to file. The drawing can be saved in any save format supported by Aspose.Diagram. For the list of all supported save formats see the [SaveFileFormat]() Enum.
## **Saving Visio Diagram**
The Diagram class of the Aspose.Diagram API represents a Visio drawing and developers can save its Visio diagram object in any supported file format. To save a Microsoft Visio file, simply use the [Diagram.Save]() method, it accepts a file name with a complete path or a file stream object. Aspose.Diagram API infers the save format from the file extension and also offers an additional SaveFileFormat parameter to specify the output file format.
### **Save a Visio Diagram in any Supported File Format**
Using Aspose.Diagram API, developers can save a Visio diagram in any supported file format as listed below:
**VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX, TIFF, PNG, BMP, EMF, JPEG, PDF, XPS, GIF, HTML, SVG, SWF and XAML**
### **Saving Diagram Programming Sample**
The example below saves a document to a file.

{{< highlight java >}}

 // Save a Visio diagram

diagram.Save(GetMyDir() + "MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Specifying Visio Save Options**
There are several [Diagram.Save]() method overloads that accept a SaveOptions object. This should be an object of a class derived from the SaveOptions class. Each save format has a corresponding class that holds save options for that save format. For example, there is PdfSaveOptions for the SaveFileFormat.PDF save format.
### **Visio Diagram Save Options**
These examples show how to:

- [Use Diagram Save Options](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Use PDF Save Options](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Use HTML Save Options](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Use Image Save Options](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Use SVG Save Options](https://docs.aspose.com/diagram/python-net/save-visio-document/).
- [Use SWF Save Options](https://docs.aspose.com/diagram/python-net/save-visio-document/).
#### **Use of the Diagram Save Options**
The code below shows how to set save options before saving a document to Visio format.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

options = saving.DiagramSaveOptions(SaveFileFormat.VSDX)

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", options)
{{< /highlight >}}




#### **Use of the PDF Save Options**
The code below shows how to set save options before saving a document to a PDF format.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
options = saving.PdfSaveOptions()
    
#// Save one page only, by page index
options.page_index = 0

#// Save diagram in the pdf format
diagram.save("CreateNewVisio_out.pdf", options)
{{< /highlight >}}




#### **Use of the HTML Save Options**
The code below shows how to set save options before saving a document to HTML file format.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
options = saving.HTMLSaveOptions()
    
#// Save one page only, by page index
options.page_index = 0

#// Save diagram in the html format
diagram.save("Visio_out.html", options)
{{< /highlight >}}




#### **Use of the Image Save Options**
The code below shows how to set save options before saving a document to image file format.




{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
#// Save diagram as PNG
options = saving.ImageSaveOptions(SaveFileFormat.PNG)
    
#// Save one page only, by page index
options.page_index = 0

#// Save diagram in the png format
diagram.save("ExportPageToImage_out.png", options)
{{< /highlight >}}



Use of the SVG Save Options

The code below shows how to set save options before saving a document to SVG format.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
#// Save diagram as svg
options = saving.SVGSaveOptions()
    
#// Save one page only, by page index
options.page_index = 0

#// Save diagram in the svg format
diagram.save("ExportPageToSvg_out.svg", options)
{{< /highlight >}}


Sometimes, developers need to save or export Visio diagrams to different file formats programmatically (like VDX, PDF, JPEG and so on).

### ` `**Saving VSD File to Other Formats with Aspose.Diagram for Python via .NET**
Using Aspose.Diagram, developers don't need Microsoft Office Visio in the machine, and they can work independently of Microsoft Office Automation.

The code snippets below show how to:

1. Load a diagram.
1. Save the diagram to VSX, PDF and JPEG.
#### **Saving VSD File with Aspose.Diagram for Python via .NET Programming Sample**
{{% alert color="primary" %}} 

import aspose.diagram
from aspose.diagram import *

{{% /alert %}} 

**Example:**


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))
#// Save the diagram as VDX
vsdDiagram.save(os.path.join(outputDir, "SaveDiagramToVDXwithAspose_out.vdx"), SaveFileFormat.VDX)

#// Save as PDF
vsdDiagram.save(os.path.join(outputDir, "SaveDiagramToPDFwithAspose_out.pdf"), SaveFileFormat.PDF)

#// Save as JPEG
vsdDiagram.save(os.path.join(outputDir, "SaveDiagramToJPGwithAspose_out.jpg"), SaveFileFormat.JPEG)
{{< /highlight >}}

