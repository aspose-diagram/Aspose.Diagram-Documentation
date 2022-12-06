---
title: Apri un disegno Visio esistente in Ruby
type: docs
weight: 90
url: /it/java/open-an-existing-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Apri un disegno Visio esistente**
 Per aprire un disegno esistente Visio utilizzando**Aspose.Diagram Java per Rubino**, puoi usare il seguente codice.

**Codice Rubino**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

{{< /highlight >}}
