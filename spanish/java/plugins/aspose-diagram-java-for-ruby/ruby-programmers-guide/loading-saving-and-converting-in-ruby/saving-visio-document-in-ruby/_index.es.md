---
title: Guardando el documento Visio en Ruby
type: docs
weight: 100
url: /es/java/saving-visio-document-in-ruby/
---
## **Aspose.Diagram - Ahorro Visio Documento**
 Para guardar el documento Visio usando**Aspose.Diagram Java para rubí**, puede usar el siguiente código.

**código rubí**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Save as VDX

diagram.save(data_dir + "Diagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

{{< /highlight >}}
