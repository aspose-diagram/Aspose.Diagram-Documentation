---
title: افتح الوثيقة Visio برمجياً
linktitle: افتح وثيقة Visio
type: docs
weight: 20
url: /ar/net/open-visio-document/
description: توضح هذه الصفحة كيفية فتح مستند Visio من البداية باستخدام مكتبة Aspose.Diagram.
---
## **اقرأ رسم Visio موجود**
Aspose.Diagram API يدعم تكوين الرسوم التخطيطية Visio الجديدة من البداية ثم الحفظ بأي تنسيق ملف مدعوم. يمكن للمطورين أيضًا تحميل Visio diagram موجود لأغراض التعديل أو الإضافة أو المعالجة.
## **قراءة Diagram**
باستخدام Aspose.Diagram API ، يمكن للمطورين تحميل كافة تنسيقات الملفات المدعومة Visio. تسمح المنشئات المتاحة لفئة Diagram بالقيام بذلك وتقبل سلسلة مسار ملف صالحة أو دفق ملف لملف المصدر Visio.

تنسيقات الملفات المدعومة القابلة للقراءة هي كما يلي:
**VSDX ، VSD ، VSDM ، VSS ، VSSX ، VSSM ، VTX ، VSTM ، VDX ، VDW ، VST ، VSTX و VSX**

يوفر مُنشئو الفئة diagram أيضًا معلمة اختيارية تحدد LoadFileFormat أو LoadOptions. إنها معلومات التحميل المسبق التي يمكن للمطورين تمريرها إلى Aspose.Diagram API. نوصي بتمرير المعلومات الواقعية للحصول على أداء مثالي.
## **قراءة Diagram عينة البرمجة**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD stream
FileStream st = new FileStream(dataDir + "Drawing1.vsdx", FileMode.Open);
Diagram vsdDiagram = new Diagram(st);
st.Close();

// Call the diagram constructor to load a VDX diagram
Diagram vdxDiagram = new Diagram(dataDir + "Drawing1.vdx");

/*
 * Call diagram constructor to load a VSS stencil
 * providing load file format
*/
Diagram vssDiagram = new Diagram(dataDir + "Basic.vss", LoadFileFormat.VSS);

/*
 * Call diagram constructor to load diagram from a VSX file
 * providing load options
*/
LoadOptions loadOptions = new LoadOptions(LoadFileFormat.VSX);
Diagram vsxDiagram = new Diagram(dataDir + "Drawing1.vsx", loadOptions);

{{< /highlight >}}
```
