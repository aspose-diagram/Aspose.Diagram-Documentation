---
title: Working with Layers
type: docs
weight: 160
url: /java/working-with-layers/
---

### **Configuring Shape Objects with Layers**
Aspose.Diagram for Java allows to configure shape objects with layers in Microsoft Office Visio diagram. Each shape can belong to multiple layers so developers can manage shapes to suit end user needs.

The [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Shape) class object offers LayerMember property which allows to add / remove shape objects to / from the layers in Visio drawing. Users can manage these properties programmatically using Aspose.Diagram API as follows:

**Add, remove and move shape objects to / from layers of the diagram.** 

![todo:image_alt_text](working-with-layers_1.png)

The following piece of code helps to add, remove and move shape objects properties.
#### **Programming Samples**
{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-Layers-ConfigureShapeLayers-ConfigureShapeLayers.java" >}}
### **Add a Layer in the Visio PageSheet**
Aspose.Diagram for Java allows developers to add new layers to organize custom categories of shapes, and then assign shapes to those layers programmatically.

The [LayerCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/LayerCollection) class offers add method which allows to add a new [Layer](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Layer) class object in the Visio drawing. Developers can set Layer properties by initializing its class object.

The following piece of code helps to add Layer objects.
#### **Programming Samples**
{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-Layers-AddLayer-AddLayer.java" >}}

{{% alert color="primary" %}} 

Aspose.Diagram for Java gives developers access to the existing layers of Visio diagram.

{{% /alert %}} 
### **Get All Available Layers**
The [PageSheet](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/PageSheet) property of the [Page](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Page) class allows to retrieve the list of available layers from the Visio diagram using [LayerCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/LayerCollection) class.

The following piece of code helps to get list of Layers.
#### **Programming Samples**
{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-Layers-RetrieveAllLayers-RetrieveAllLayers.java" >}}
