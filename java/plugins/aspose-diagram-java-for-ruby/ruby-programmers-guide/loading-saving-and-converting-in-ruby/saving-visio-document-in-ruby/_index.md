---
title: Saving Visio Document in Ruby
type: docs
weight: 100
url: /java/saving-visio-document-in-ruby/
---

## **Aspose.Diagram - Saving Visio Document**
To Save Visio Document using **Aspose.Diagram Java for Ruby**, you can use following code.

**Ruby Code**

{{< highlight ruby >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Save as VDX

diagram.save(data_dir + "Diagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

{{< /highlight >}}
