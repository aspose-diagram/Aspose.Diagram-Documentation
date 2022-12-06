---
title: Abra un dibujo Visio existente en Ruby
type: docs
weight: 90
url: /es/java/open-an-existing-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Abrir un dibujo Visio existente**
 Para abrir un dibujo Visio existente usando**Aspose.Diagram Java para rubí**, puede usar el siguiente código.

**código rubí**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

{{< /highlight >}}
