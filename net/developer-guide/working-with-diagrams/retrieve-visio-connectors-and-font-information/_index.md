---
title: Retrieve Visio Connectors and Font Information
type: docs
weight: 20
url: /net/retrieve-visio-connectors-and-font-information/
description:This section explains how to get visio connectors and font information.
---

## **Retrieving Connector Information**
Aspose.Diagram for .NET provides mechanisms for retrieving information - ID and name - about [pages](/diagram/net/retrieve-2c-get-2c-copy-and-insert-a-page/) and [master](https://docs.aspose.com/diagram/net/working-with-masters/). It also lets you get information about connectors, the elements that link shapes.

The [Connect](http://www.aspose.com/api/net/diagram/aspose.diagram/connect) object represents a connector that joins two shapes on a Visio drawing page. The Connects property, exposed by the [Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class supports a collection of Aspose.Diagram.Connect objects. This property can be used to retrieve ID and name information about a connector.
### **Programming Sample**
The following piece of code retrieves the information for the connectors in a diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RetrieveConnectorInfo-RetrieveConnectorInfo.cs" >}}
## **Retrieving Font Information**
Aspose.Diagram has mechanisms for retrieving information about the elements that make up a diagram, from [pages](/diagram/net/retrieve-2c-get-2c-copy-and-insert-a-page/), [stencils](https://docs.aspose.com/diagram/net/working-with-masters/), [connectors](/diagram/net/retrieving-connector-information/) and also fonts. This article shows how to find out which fonts are used in a diagram.

The [Font](http://www.aspose.com/api/net/diagram/aspose.diagram/font) object represents a typeface that is either applied to text in a document or available for use on the system. A Font object maps a name (for example, "Arial") to the font ID (for example, 3) that Microsoft Visio stores in a Font cell in a Character section of a shape that contains text formatted with that font. Font IDs can change when a document is opened on different systems or when fonts are installed or removed.
### **Retrieving Font Programming Sample**
The following piece of code retrieves font information from the Visio diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RetrieveFontInfo-RetrieveFontInfo.cs" >}}
### **Getting Default Font Directory**
Aspose.Diagram for .NET API also allows getting default font directory path using GetDefaultFontDir() method of Diagram Class. The following piece of code retrieves default font directory from the Visio diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-GetDefaultFontDirectory-GetDefaultFontDirectory.cs" >}}
### **Getting Unused Fonts**
{{% alert color="primary" %}}

This method is supported by version 19.6 or greater.

{{% /alert %}}

Aspose.Diagram for .NET API also allows getting unused fonts using GetUnusedStyles() method of Diagram Class. The following piece of code retrieves unused fonts from the Visio diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-GetUnusedFonts-1.cs" >}}
