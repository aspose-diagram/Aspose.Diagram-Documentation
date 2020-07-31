---
title : "Retrieve Visio Connectors and Font Information" 
description : "" 
weight : 12020 
toc : false
type: docs
url: /net/developerguide/workingwithdiagrams/retrieve+visio+connectors+and+font+information/
---

# Aspose.Diagram for .NET : Retrieve Visio Connectors and Font Information


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Retrieving Connector Information](#retrieving-connector-information)
    *   1.1 [Programming Sample](#programming-sample)
*   2 [Retrieving Font Information](#retrieving-font-information)
    *   2.1 [Retrieving Font Programming Sample](#retrieving-font-programming-sample)
    *   2.2 [Getting Default Font Directory](#getting-default-font-directory)
    *   2.3 [Getting Unused Fonts](#getting-unused-fonts)
{{< /panel >}}
 

 

## Retrieving Connector Information

Aspose.Diagram for .NET provides mechanisms for retrieving information - ID and name - about [pages](https://docs2.aspose.com/diagram/net/developerguide/workingwithpages/retrieve+get+copy+and+insert+a+page) and [master](http://www.aspose.com/docs/display/diagramnet/Working+with+Masters#WorkingwithMasters-RetrievingMasterInformation). It also lets you get information about connectors, the elements that link shapes.

The [Connect](http://www.aspose.com/api/net/diagram/aspose.diagram/connect) object represents a connector that joins two shapes on a Visio drawing page. The `Connects` property, exposed by the [`Page`](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class supports a collection of `Aspose.Diagram.Connect` objects. This property can be used to retrieve ID and name information about a connector.

### Programming Sample

The following piece of code retrieves the information for the connectors in a diagram.

## Retrieving Font Information

Aspose.Diagram has mechanisms for retrieving information about the elements that make up a diagram, from [pages](https://docs2.aspose.com/diagram/net/developerguide/workingwithpages/retrieve+get+copy+and+insert+a+page), [stencils](http://www.aspose.com/docs/display/diagramnet/Working+with+Masters#WorkingwithMasters-RetrievingMasterInformation), [connectors](https://docs2.aspose.com/diagram/net/plugins/vsto/codecomparison/retrieving+connector+information) and also fonts. This article shows how to find out which fonts are used in a diagram.

The [Font](http://www.aspose.com/api/net/diagram/aspose.diagram/font) object represents a typeface that is either applied to text in a document or available for use on the system. A `Font` object maps a name (for example, "Arial") to the font ID (for example, 3) that Microsoft Visio stores in a `Font` cell in a `Character` section of a shape that contains text formatted with that font. Font IDs can change when a document is opened on different systems or when fonts are installed or removed.

### Retrieving Font Programming Sample

The following piece of code retrieves font information from the Visio diagram.

### Getting Default Font Directory

Aspose.Diagram for .NET API also allows getting default font directory path using `GetDefaultFontDir()` method of `Diagram` Class. The following piece of code retrieves default font directory from the Visio diagram.

### Getting Unused Fonts

This method is supported by version 19.6 or greater.

Aspose.Diagram for .NET API also allows getting unused fonts using `GetUnusedStyles()` method of `Diagram` Class. The following piece of code retrieves unused fonts from the Visio diagram.

