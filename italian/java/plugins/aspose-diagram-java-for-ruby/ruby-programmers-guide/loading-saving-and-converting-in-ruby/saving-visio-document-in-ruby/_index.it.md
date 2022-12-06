---
title: Salvataggio del documento Visio in Ruby
type: docs
weight: 100
url: /it/java/saving-visio-document-in-ruby/
---
## **Aspose.Diagram - Salvataggio documento Visio**
 Per salvare il documento Visio utilizzando**Aspose.Diagram Java per Rubino**, puoi usare il seguente codice.

**Codice Rubino**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Save as VDX

diagram.save(data_dir + "Diagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

{{< /highlight >}}
