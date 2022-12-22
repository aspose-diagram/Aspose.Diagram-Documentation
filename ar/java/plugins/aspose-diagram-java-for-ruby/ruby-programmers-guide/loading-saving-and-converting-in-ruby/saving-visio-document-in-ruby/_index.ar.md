---
title: حفظ مستند Visio في روبي
type: docs
weight: 100
url: /ar/java/saving-visio-document-in-ruby/
---
## **Aspose.Diagram - حفظ Visio وثيقة**
 لحفظ Visio المستند باستخدام**Aspose.Diagram Java لروبي**، يمكنك استخدام الكود التالي.

**كود روبي**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Save as VDX

diagram.save(data_dir + "Diagram.vdx", Rjb::import('com.aspose.diagram.SaveFileFormat').VDX)

{{< /highlight >}}
