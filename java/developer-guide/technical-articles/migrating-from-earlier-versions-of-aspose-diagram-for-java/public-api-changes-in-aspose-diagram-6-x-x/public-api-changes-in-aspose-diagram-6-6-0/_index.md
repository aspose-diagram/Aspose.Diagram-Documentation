---
title: Public API Changes in Aspose.Diagram 6.6.0
type: docs
weight: 30
url: /java/public-api-changes-in-aspose-diagram-6-6-0/
---

{{% alert color="primary" %}} 

This document describes changes to the Aspose.Diagram API from version 6.3.0 to 6.6.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.Diagram. 

{{% /alert %}} 
### **Adds VSDM, VSSM and VSTM formats in LoadFileFormat class**
This version adds support of reading macro-enabled Visio formats.
### **Adds VSDM, VSSM and VSTM formats in SaveFileFormat class**
This version adds support of writing macro-enabled Visio formats.
### **Modify VBA Module Code in Visio Diagram**
We have added Vba, VbaProject and VbaModule classes. These classes help to get control over VBA project. Using this new version 6.6.0 or higher, developers can extract and modify VBA module code. Please check this code example:

**Java**

{{< highlight java >}}

 // load an existing Visio diagram

InputStream input = new FileInputStream("c:\\temp\\macro.vsdm");

Diagram diagram = new Diagram(input);

// extract VBA project

VbaProject v = diagram.getVbaProject();

// Iterate through the modules and modify VBA macro code

for (int i=0;i< diagram.getVbaProject().getModules().getCount();i++)

{

    VbaModule module =  diagram.getVbaProject().getModules().get(i);

    String code = module.getCodes();

    if (code.contains("This is test message."))

        code = code.replace("This is test message.", "This is Aspose.Diagram message.");

    module.setCodes (code);

}

// save the Visio diagram

diagram.Save("c:\\temp\\out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}
### **Adds a getImageData Method in ForeignData class**
It represents an image of ole object as a byte array. Besides this, we have also enhanced the manipulation of OLE objects. Developers can now also replace an OLE object in the Visio diagram. Please check this code example:

**Java**

{{< highlight java >}}

 String DirPath = "c:\\temp\\";

// load a Visio diagram

Diagram diagram = new Diagram(DirPath + "Drawing1.vsdx");

// get page of the Visio diagram by name

Page page = diagram.getPages().getPage("Page-1");

// get shape of the Visio diagram by ID

Shape OLE_Shape = page.getShapes().getShape(2);

// filter shapes by type Foreign

if (OLE_Shape.getType() == TypeValue.FOREIGN)

{

    if (OLE_Shape.getForeignData().getForeignType() == ForeignType.OBJECT)

    {

    	ByteArrayInputStream Ole_stream = new ByteArrayInputStream(OLE_Shape.getForeignData().getObjectData());

        // get format of the OLE file object

        com.aspose.words.FileFormatInfo info = com.aspose.words.FileFormatUtil.detectFileFormat(Ole_stream);

        if (info.getLoadFormat() == com.aspose.words.LoadFormat.DOC || info.getLoadFormat() == com.aspose.words.LoadFormat.DOCX)

        {

            // modify an OLE object

            com.aspose.words.Document doc = new com.aspose.words.Document(new ByteArrayInputStream(OLE_Shape.getForeignData().getObjectData()));

    	    doc.getRange().replace("testing", "Aspose", false, true);

            ByteArrayOutputStream outStream = new ByteArrayOutputStream();

            doc.save(outStream, com.aspose.words.SaveFormat.DOCX);

            // seve an OLE object

            OLE_Shape.getForeignData().setObjectData(outStream.toByteArray());

        }

    }

}

// save Visio diagram

diagram.save(DirPath + "modified.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
