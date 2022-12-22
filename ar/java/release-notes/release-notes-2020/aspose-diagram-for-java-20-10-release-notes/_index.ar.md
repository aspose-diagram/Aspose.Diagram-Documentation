---
title: Aspose.Diagram for Java 20.10 ملاحظات الإصدار
type: docs
weight: 10
url: /ar/java/aspose-diagram-for-java-20-10-release-notes/
---
{{% alert color="primary" %}}

تحتوي هذه الصفحة على معلومات حول ملاحظات الإصدار Aspose.Diagram for Java 20.10.

{{% /alert %}}
## **التحسينات والتغييرات**  ##

|**مفتاح**|**ملخص**|**فئة**|
|:- |:- |:- |
|DIAGRAMJAVA-50457|يتم إزاحة عناصر النص عند تحويل صفحات VSD إلى SVGs|التعزيز|

## التغييرات العامة API
* تمت إضافة IsExportScaleInMatrix في SVGSaveOptions - يحدد ما إذا كنت بحاجة إلى نطاق تصدير في المصفوفة أم لا.
```
SVGSaveOptions o = new SVGSaveOptions();
o.setExportScaleInMatrix(false);
```
