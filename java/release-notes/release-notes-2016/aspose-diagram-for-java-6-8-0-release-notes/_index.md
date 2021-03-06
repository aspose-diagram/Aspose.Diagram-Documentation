---
title: Aspose.Diagram for Java 6.8.0 Release Notes
type: docs
weight: 40
url: /java/aspose-diagram-for-java-6-8-0-release-notes/
---

{{% alert color="primary" %}} 

This page contains release notes for [Aspose.Diagram for Java 6.8.0](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-diagram/6.8.0/).

{{% /alert %}} 
## **Other Improvements and Changes**

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|DIAGRAMJAVA-50347|Add support of inserting ActiveX controls in the Visio Page.|New Feature|
|DIAGRAMJAVA-50360|Add support to set color checkbox of the layer.|New Feature|
|DIAGRAMJAVA-50348|Can't copy a Visio page in the VSDM.|Enhancement|
|DIAGRAMJAVA-50357|The incomplete rendering of an OLE chart when converting a VSDX to PDF.|Enhancement|
|DIAGRAMJAVA-50358|An OLE chart is not being rendered on converting a VSDX to PNG.|Enhancement|
|DIAGRAMJAVA-50207|VSDX to PDF conversion, the embedded word document icon is missing.|Bug|
|DIAGRAMJAVA-50346|Incorrect retrieval of the Connects from a VSD.|Bug|
|DIAGRAMJAVA-50349|Returns junk value of fill pattern color of each shape.|Bug|
|DIAGRAMJAVA-50350|Incomplete rendering of a dynamic connector in the VSDM diagram.|Bug|
|DIAGRAMJAVA-50354|A blank PDF is generated while converting a VSDX to PDF.|Bug|
|DIAGRAMJAVA-50355|An author list error occurred while loading a VSDX.|Bug|
|DIAGRAMJAVA-50359|Retrieves a reverse direction of the connector from a VSD diagram.|Bug|
|DIAGRAMJAVA-50362|Returns incorrect connections, while retrieving from a VSD.|Bug|
### **Public API and Backwards Incompatible Changes**
See the list for any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.Diagram for Java. If you have concerns about any change listed, please raise it on the [Aspose.Diagram support forum](http://www.aspose.com/community/forums/aspose.diagram-product-family/489/showforum.aspx).
### **Adds addActiveXControl Method in the Page Class**
It creates an ActiveX Control in the Visio diagram.
### **Adds setColorChecked Method and isColorChecked Property in the Layer Class**
A flag indicating whether the element has been checked locally.
### **Adds getInheritFill Method in Shape Class**
It contains the fill formatting values for the shape inherit by the parent style and the master shape.
### **Usage Examples**
Please check the list of help topics added in the Aspose.Diagram Wiki docs:

- [Add a new Layer in the Visio Page](http://www.aspose.com/docs/display/diagramjava/Working+with+Layers#WorkingwithLayers-AddaLayerintheVisioPageSheet)
- [Insert an ActiveX Control in the Visio Diagram](http://www.aspose.com/docs/display/diagramjava/Insert+an+ActiveX+Control+in+the+Visio+Diagram)
- [Read Inherited Fill Data of a Visio Shape](http://www.aspose.com/docs/display/diagramjava/Set+Visio+Shape%27s+XForm%2C+Line+and+Fill+Data#SetVisioShape%27sXForm%2CLineandFillData-RetrieveInheritedFillDataofaVisioShape)
