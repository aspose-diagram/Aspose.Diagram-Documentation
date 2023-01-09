---
title: Öppna en befintlig Visio-ritning i Ruby
type: docs
weight: 90
url: /sv/java/open-an-existing-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Öppna en befintlig Visio ritning**
 För att öppna en befintlig Visio Ritning med hjälp av**Aspose.Diagram Java för Ruby**, kan du använda följande kod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

{{< /highlight >}}
