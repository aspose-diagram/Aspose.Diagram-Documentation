---
title: Working with Layers
type: docs
weight: 130
url: /net/working-with-layers/
description: This section explains how to add or get layer information in a visio shape with Aspose.Diagram.
---

## **Configure Shape Objects with Layers in Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) allows to configure shape objects with layers in Microsoft Office Visio diagram. Each shape can belong to multiple layers so developers can manage shapes to suit end user needs. The [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class object offers LayerMember property which allows to add and remove shape objects to and from the layers in Visio drawing. Users can manage these properties programmatically using Aspose.Diagram API as follows:
### **Configure Shape Objects Programming Sample**
The following piece of code helps to add, remove and move shape object properties.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Layers-ConfigureShapeLayers-ConfigureShapeLayers.cs" >}}
## **Add a new Layer in the Visio Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) allows developers to add new layers to organize custom categories of shapes, and then assign shapes to those layers programmatically. The [LayerCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) class offers Add method which allows to add a new [Layer](http://www.aspose.com/api/net/diagram/aspose.diagram/layer) in the Visio drawing. Developers can set Layer properties by initializing its class object.
### **Add Layer Programming Sample**
The following piece of code helps to add Layer objects.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Layers-AddLayer-AddLayer.cs" >}}
## **Retrieve All Layers from the Visio Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) gives access to developers to get the existing layers of a Visio diagram. The [PageSheet](http://www.aspose.com/api/net/diagram/aspose.diagram/pagesheet) property of the [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class allows to retrieve the list of available layers from a Visio diagram using [LayerCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) class.
### **Retrieve Layers Programming Sample**
The following piece of code helps to get the list of Layers.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Layers-RetrieveAllLayers-RetrieveAllLayers.cs" >}}
