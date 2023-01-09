---
title: Speichern des Visio-Dokuments in Ruby
type: docs
weight: 100
url: /de/java/saving-visio-document-in-ruby/
---
## **Aspose.Diagram - Speichern des Visio-Dokuments**
 Zum Speichern von Visio-Dokumenten mit**Aspose.Diagram Java für Rubin**, können Sie folgenden Code verwenden.

**Ruby-Code**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Save as VDX

diagram.save(data_dir + "Diagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

{{< /highlight >}}
