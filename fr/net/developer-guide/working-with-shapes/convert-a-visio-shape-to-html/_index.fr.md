---
title: Convertir une forme Visio en HTML
type: docs
weight: 10
url: /fr/net/convert-a-visio-shape-to-html/
description: Cette section explique comment convertir une forme visio en html avec Aspose.Diagram.
---
## ** Convertir une forme visio en html**
 La méthode ToHTML exposée par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class peut être utilisé pour convertir en html.

Le code ci-dessous montre comment :

1. Charger un échantillon diagram.
1. obtenir une page particulière.
1. obtenir une forme particulière.
1. convertir la forme en html.
### **Forme en Html**
Utilisez le code suivant dans votre application .net pour convertir une forme visio en html.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Call a Diagram class constructor to load the VSDX diagram
Diagram diagram = new Diagram(dataDir + "ShapeToHtml.vsdx");

// Get a particular page
Page page = diagram.Pages[0];

// Get a particular shape
Shape shape = page.Shapes[0];

// Shape to HTML
Aspose.Diagram.Saving.HTMLSaveOptions hs = new Aspose.Diagram.Saving.HTMLSaveOptions();
shape.ToHTML("out.htm", hs);

{{< /highlight >}}
```

