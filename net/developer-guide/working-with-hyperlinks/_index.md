---
title: Working with Hyperlinks
type: docs
weight: 160
url: /net/working-with-hyperlinks/
---

## **Add Hyperlink to a Visio Shape**
Microsoft Office Visio supports adding the hyperlinks to any shape. The hyperlinks can link to another page or shape in the current drawing, a page or shape in another drawing, a document other than a Visio drawing, a Web site, FTP site, or e-mail address. Developers can use Aspose.Diagram API to easily add hyperlinks to a Visio shape.

In the multi page Visio drawing, hyperlinks can navigate you from one shape to many other types of the links. [HyperlinkCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/hyperlinkcollection) exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class offers Add method which can be used to add a shape's hyperlink.

To identify properties in Microsoft Office Visio:

1. In a Visio diagram, right-click a shape.
1. Select **Hyperlink.**
1. Set existing properties
1. Press **OK** button

**A shape's hyperlink data, as seen in Microsoft Visio**

![todo:image_alt_text](working-with-hyperlinks_1.png)
### **Add Hyperlink Programming Sample**
The code snippet below adds shape's hyperlink data.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Hyperlinks-AddHyperlinkToShape-AddHyperlinkToShape.cs" >}}
## **Get Hyperlinks Data of the Visio Shapes**
Developers can retrieve all hyperlinks from a Visio shape in the same way as they [read Visio shape data](https://docs.aspose.com/diagram/net/load-or-create-a-visio-drawing/) using [Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net).

In the multi page Visio drawing, hyperlinks can navigate you from one shape to many other types of the links. [HyperlinkCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/hyperlinkcollection) exposed by the [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class allows developers to retrieve hyperlinks.

To identify properties in Microsoft Office Visio:

1. In a diagram, right-click a shape.
1. Select **Hyperlink.**

Any existing properties are listed in the dialog.
**A shape's hyperlink data, as seen in Microsoft Visio**

![todo:image_alt_text](working-with-hyperlinks_1.png)

**A console window showing the shape data output**

![todo:image_alt_text](working-with-hyperlinks_3.png)
### **Get Hyperlinks Programming Sample**
The code snippet below reads shape's hyperlink data.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Hyperlinks-GetHyperlinks-GetHyperlinks.cs" >}}
