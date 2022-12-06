---
title: افتح رسم Visio موجود في ياقوت
type: docs
weight: 90
url: /ar/java/open-an-existing-visio-drawing-in-ruby/
---
## **Aspose.Diagram - افتح رسم Visio موجود**
 لفتح رسم Visio موجود باستخدام**Aspose.Diagram Java لروبي**، يمكنك استخدام الكود التالي.

**كود روبي**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

{{< /highlight >}}
