---
title: API العام التغييرات في Aspose.Diagram 6.7.0
type: docs
weight: 20
url: /ar/java/public-api-changes-in-aspose-diagram-6-7-0/
---
{{% alert color="primary" %}} 

يصف هذا المستند التغييرات التي تم إجراؤها على Aspose.Diagram API من الإصدار 6.6.0 إلى 6.7.0 ، والتي قد تهم مطوري الوحدة النمطية / التطبيق. لا يشمل فقط الأساليب العامة الجديدة والمحدثة ، بل يشمل أيضًا وصفًا لأي تغييرات في السلوك خلف الكواليس في Aspose.Diagram.

{{% /alert %}} 
### **يضيف طريقة detfileFormat في فئة FileFormatUtil**
يقوم باكتشاف وإرجاع المعلومات الخاصة بتنسيق Visio diagram المخزن في تدفق الإدخال. الرجاء التحقق من مثال هذا الرمز:

**Java**

{{< highlight "java" >}}

 String dataDir = "c:\\temp\\";

// Open the stream. Read only access to load a Visio diagram.

InputStream stream = new FileInputStream(dataDir + "Drawing1.vsdx");

// detect file format using an input stream

FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format

System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}
