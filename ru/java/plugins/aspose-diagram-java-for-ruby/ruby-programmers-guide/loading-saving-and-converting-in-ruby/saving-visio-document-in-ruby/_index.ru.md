---
title: Сохранение документа Visio в Ruby
type: docs
weight: 100
url: /ru/java/saving-visio-document-in-ruby/
---
## **Aspose.Diagram - Сохранение Visio Документ**
 Чтобы сохранить документ Visio, используя**Aspose.Diagram Java для рубина**, вы можете использовать следующий код.

**Рубиновый код**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Save as VDX

diagram.save(data_dir + "Diagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

{{< /highlight >}}
