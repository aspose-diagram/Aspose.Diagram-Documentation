---
title: Ouvrir un dessin Visio existant dans Ruby
type: docs
weight: 90
url: /fr/java/open-an-existing-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Ouvrir un dessin Visio existant**
 Pour ouvrir un dessin Visio existant à l'aide de**Aspose.Diagram Java pour rubis**, vous pouvez utiliser le code suivant.

**Code rubis**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

{{< /highlight >}}
