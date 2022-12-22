---
title: Visio Belgesini Ruby'ye Kaydetme
type: docs
weight: 100
url: /tr/java/saving-visio-document-in-ruby/
---
## **Aspose.Diagram - Visio Belgesi kaydediliyor**
 Kaydetmek için Visio Belgeyi kullanarak**Yakut için Aspose.Diagram Java**, aşağıdaki kodu kullanabilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Save as VDX

diagram.save(data_dir + "Diagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

{{< /highlight >}}
