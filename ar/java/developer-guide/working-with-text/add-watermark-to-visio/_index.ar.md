---
title: أضف العلامة المائية إلى Visio
type: docs
weight: 10
url: /ar/java/add-watermark-to-visio/
keywords: watermark, visi
description: كيفية إضافة العلامة المائية إلى visio باستخدام Java Diagram API.
---
## **إنشاء Diagram**
 يتيح لك Aspose.Diagram for Java قراءة وإنشاء Microsoft Visio الرسوم التخطيطية من داخل التطبيقات الخاصة بك ، بدون أتمتة Microsoft Office. الخطوة الأولى عند تكوين وثائق جديدة هي تكوين diagram. ثم[إضافة الأشكال والموصلات](https://docs.aspose.com/diagram/java/add-retrieve-copy-and-read-visio-shape-data/)لإنشاء diagram. استخدم المُنشئ الافتراضي لـ[Diagram](http://www.aspose.com/api/java/diagram/com.aspose.diagram/diagram) فئة لإنشاء diagram جديد.
### **عينة البرمجة**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateDiagram.class);
// Create directory if it is not already present.
File file = new File(dataDir);
if (!file.exists())
	file.mkdir();
// initialize a new Diagram
Diagram diagram = new Diagram();
// save in the VSDX format
diagram.save(dataDir + "CreateDiagram_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. أضف العلامة المائية إلى visio في الصفحة
1. استدعاء طريقة حفظ لكائن الفئة Diagram وأيضا تمرير مسار الملف الكامل وكائن DiagramSaveOptions.
### **أضف عينة برمجة العلامة المائية**
يوضح رمز المثال التالي كيفية إضافة علامة مائية في Visio diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddWatermarkToVisio.class);   
        
// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");

double pinx = page.getPageSheet().getPageProps().getPageWidth().getValue() / 2;
double piny = page.getPageSheet().getPageProps().getPageHeight().getValue() / 2;
double width = page.getPageSheet().getPageProps().getPageWidth().getValue();
double height =page.getPageSheet().getPageProps().getPageHeight().getValue();
    
//Add watermark
Shape shape = page.addText(pinx, piny, width, height, "Test text","Calibri","#a5a5a5",0.25);

// save diagram
diagram.save(dataDir + "ApplyFontOnText_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
