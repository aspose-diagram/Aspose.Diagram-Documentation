---
title: Sparar Visio Dokument i Ruby
type: docs
weight: 100
url: /sv/java/saving-visio-document-in-ruby/
---
## **Aspose.Diagram - Sparar Visio Dokument**
 För att spara Visio Dokument med hjälp av**Aspose.Diagram Java för Ruby**, kan du använda följande kod.

**Ruby kod**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Save as VDX

diagram.save(data_dir + "Diagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

{{< /highlight >}}
