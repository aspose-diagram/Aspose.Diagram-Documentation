---
title: Öffnen Sie eine vorhandene Visio-Zeichnung in Ruby
type: docs
weight: 90
url: /de/java/open-an-existing-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Öffnen Sie eine vorhandene Visio-Zeichnung**
 So öffnen Sie eine vorhandene Visio-Zeichnung mit**Aspose.Diagram Java für Rubin**, können Sie folgenden Code verwenden.

**Ruby-Code**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

{{< /highlight >}}
