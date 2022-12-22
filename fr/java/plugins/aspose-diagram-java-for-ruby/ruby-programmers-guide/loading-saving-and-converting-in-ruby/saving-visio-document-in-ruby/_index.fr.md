---
title: Enregistrement du document Visio en Ruby
type: docs
weight: 100
url: /fr/java/saving-visio-document-in-ruby/
---
## **Aspose.Diagram - Enregistrement Visio Document**
 Pour enregistrer le document Visio à l'aide de**Aspose.Diagram Java pour rubis**, vous pouvez utiliser le code suivant.

**Code rubis**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Save as VDX

diagram.save(data_dir + "Diagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

{{< /highlight >}}
