---
title: Working With OLE Objects
type: docs
weight: 220
url: /java/working-with-ole-objects/
---

{{% alert color="primary" %}} 

Microsoft Office Visio supports manipulating the OLE objects in the Visio diagram. If an Excel spreadsheet or any other file resides outside of the Visio drawing and developers need to add a feature in their Java applications to auto insert these files inside of the drawing, they can achieve this by using [Aspose.Diagram for Java API](http://www.aspose.com/products/diagram/java).

{{% /alert %}} 
### **Manipulate the Embedded OLE Objects Programming Sample**
ObjectData property of the ForeignData class allows developers to manipulate with existing OLE objects in Visio diagram. This help topic demonstrates how developers can retrieve an OLE object of the Word document, edit it using [Aspose.Words for Java API](http://www.aspose.com/products/words/java), and then save back as an OLE object in the Visio diagram.

{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-OLEObjectsinVisioDiagram-ManipulateEmbeddedOLEObjects-ManipulateEmbeddedOLEObjects.java" >}}
