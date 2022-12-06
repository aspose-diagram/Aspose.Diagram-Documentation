---
title: Open an Existing Visio Drawing in Ruby
type: docs
weight: 90
url: /java/open-an-existing-visio-drawing-in-ruby/
---

## **Aspose.Diagram - Open an Existing Visio Drawing**
To Open an Existing Visio Drawing using **Aspose.Diagram Java for Ruby**, you can use following code.

**Ruby Code**

{{< highlight ruby >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

{{< /highlight >}}
