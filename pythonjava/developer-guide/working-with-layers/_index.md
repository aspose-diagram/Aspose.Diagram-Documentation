---
title: Working with Layers
type: docs
weight: 160
url: /python-java/working-with-layers/
---

### **Configuring Shape Objects with Layers**
Aspose.Diagram for Python via Java allows to configure shape objects with layers in Microsoft Office Visio diagram. Each shape can belong to multiple layers so developers can manage shapes to suit end user needs.

The [Shape](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape) class object offers LayerMember property which allows to add / remove shape objects to / from the layers in Visio drawing. Users can manage these properties programmatically using Aspose.Diagram API as follows:

**Add, remove and move shape objects to / from layers of the diagram.** 

The following piece of code helps to add, remove and move shape objects properties.
#### **Programming Samples**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-ConfigureShapeLayers.py" >}}
### **Add a Layer in the Visio PageSheet**
Aspose.Diagram for Python via Java allows developers to add new layers to organize custom categories of shapes, and then assign shapes to those layers programmatically.

The [LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection) class offers add method which allows to add a new [Layer](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer) class object in [the Visio drawing](DrawingFlowChart.vsdx). Developers can set Layer properties by initializing its class object.

The following piece of code helps to add Layer objects.
#### **Programming Samples**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-AddLayer.py" >}}

{{% alert color="primary" %}} 

Aspose.Diagram for Python via Java gives developers access to the existing layers of Visio diagram.

{{% /alert %}} 
### **Get All Available Layers**
The [PageSheet](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet) property of the [Page](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) class allows to retrieve the list of available layers from [the Visio drawing](DrawingFlowChart.vsdx) using [LayerCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection) class.

The following piece of code helps to get list of Layers.
#### **Programming Samples**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-RetrieveAllLayers.py" >}}
