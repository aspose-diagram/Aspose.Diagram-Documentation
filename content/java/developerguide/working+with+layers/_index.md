---
title : "Working with Layers" 
description : "" 
weight : 8049 
toc : false
type: docs
url: /java/developerguide/working+with+layers/
---

# Aspose.Diagram for Java : Working with Layers


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Configuring Shape Objects with Layers](#configuring-shape-objects-with-layers)
    *   1.1 [Programming Samples](#programming-samples)
*   2 [Add a Layer in the Visio PageSheet](#add-a-layer-in-the-visio-pagesheet)
    *   2.1 [Programming Samples](#programming-samples)
*   3 [Get All Available Layers](#get-all-available-layers)
    *   3.1 [Programming Samples](#programming-samples)
{{< /panel >}}
 

 

### Configuring Shape Objects with Layers

Aspose.Diagram for Java allows to configure shape objects with layers in Microsoft Office Visio diagram. Each shape can belong to multiple layers so developers can manage shapes to suit end user needs.

The [Shape](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Shape) class object offers LayerMember property which allows to add / remove shape objects to / from the layers in Visio drawing. Users can manage these properties programmatically using Aspose.Diagram API as follows:

**Add, remove and move shape objects to / from layers of the diagram.**  
![image](https://docs2.aspose.com/diagram/java/attachments/18612547/18809096.png)

The following piece of code helps to add, remove and move shape objects properties.

#### Programming Samples

### Add a Layer in the Visio PageSheet

Aspose.Diagram for Java allows developers to add new layers to organize custom categories of shapes, and then assign shapes to those layers programmatically.

The [LayerCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/LayerCollection) class offers add method which allows to add a new [Layer](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Layer) class object in the Visio drawing. Developers can set `Layer` properties by initializing its class object.

The following piece of code helps to add `Layer` objects.

#### Programming Samples

Aspose.Diagram for Java gives developers access to the existing layers of Visio diagram.

### Get All Available Layers

The [PageSheet](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/PageSheet) property of the [Page](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Page) class allows to retrieve the list of available layers from the Visio diagram using [LayerCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/LayerCollection) class.

The following piece of code helps to get list of `Layers`.

#### Programming Samples

