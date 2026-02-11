---
title: العمل مع الحماية
type: docs
weight: 170
url: /ar/net/working-with-protection/
description: يشرح هذا القسم كيفية ضبط الحماية في diagram مع Aspose.Diagram.
---
## **مجموعة حماية Visio Diagram**
 تسمح حماية الرسوم التخطيطية للمستخدمين بقفل الخلفيات والماجستير (الإستنسل) والأشكال والأنماط بحيث لا يمكن تحريرها. يفيد ذلك في حماية أنماط الشركة ، على سبيل المثال ، وضمان الحصول على مظهر متناسق عبر مجموعة من الرسوم التخطيطية. يمكن للمطورين تحقيق ذلك باستخدام[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **قم بتحرير حماية Visio Diagram**
خصائص ProtectBkgnds و ProtectMasters و ProtectShapes و ProtectStyles التي يتعرض لها[إعدادات المستند](http://www.aspose.com/api/net/diagram/aspose.diagram/documentsettings) فئة تدعم كائن Aspose.Diagram.BoolValue. يمكن استخدام هذه الخصائص لحماية الرسوم التخطيطية Microsoft Office Microsoft وإلغاء حمايتها. في Microsoft Visio تقوم بحماية المستندات بهذه الطريقة:

1. افتح diagram في Microsoft Visio.
1. افتح نافذة مستكشف الرسم.
1.  انقر بزر الماوس الأيمن فوق diagram وحدد**حماية المستند** من القائمة.
1. في نافذة حماية المستند ، حدد الخيارات أو امسحها لقفل أو إلغاء قفل عناصر diagram مختلفة.
1.  انقر**نعم**.
#### **قم بتحرير نموذج برمجة الحماية Diagram**
استخدم الكود أدناه في تطبيق .NET لأداء نفس المهام مثل قفل وفتح عناصر مختلفة من Visio diagram باستخدام Aspose.Diagram for .NET API.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Protection();

// Load diagram
Diagram diagram = new Diagram(dataDir + "ProtectAndUnprotect.vsd");

diagram.DocumentSettings.ProtectBkgnds = BOOL.True;
diagram.DocumentSettings.ProtectMasters = BOOL.True;
diagram.DocumentSettings.ProtectShapes = BOOL.True;
diagram.DocumentSettings.ProtectStyles = BOOL.True;
// Save diagram
diagram.Save(dataDir + "VisioDiagramProtection_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
## **تعيين الحماية للشكل Visio**
 تسمح حماية الأشكال Visio للمستخدمين بقفل جوانب معينة من الأشكال. تشمل جوانب الأشكال التي يمكن تأمينها من خلال حماية الشكل العرض والارتفاع وموضع x وموضع y والدوران والمزيد. يمكن للمطورين تحقيق ذلك باستخدام[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **قم بتحرير حماية الشكل Visio**
**LockAspect**, **LockBegin**, **LockCalcWH**, **LockCrop**, **LockCustProp**, **قفل حذف**, **LockEnd**, **القفل**, **LockFromGroupFormat**, **لوكجروب**, **ارتفاع القفل**, **LockMoveX**, **LockMoveY**, **LockRotate**, **القفل**, **LockTextEdit**, **LockThemeColors**, **قفل التأثيرات**, **LockVtxEdit** و**عرض القفل** خصائص مكشوفة بواسطة[**حماية**](http://www.aspose.com/api/net/diagram/aspose.diagram/Protection) فئة دعم**Aspose.Diagram.BoolValue** هدف. يمكن استخدام هذه الخصائص لحماية الأشكال وإلغاء حمايتها.

في Microsoft Office Visio ، يمكن للمستخدم القيام بالإجراءات التالية لحماية أي شكل:

- افتح diagram في Microsoft Office Visio
- حدد أي شكل
- حدد "حماية ..." من قائمة "تنسيق" إذا كنت تستخدم Visio 2007 أو حدد "حماية" من قائمة "المطور" إذا كنت تستخدم Visio 2010
- في نافذة "الحماية" ، حدد / ألغِ تحديد أي مربع نص لقفل أو إلغاء قفل أي سمة للشكل
- اضغط موافق'
### **قم بتحرير نموذج برمجة حماية الشكل**
استخدم الكود التالي في تطبيق .NET الخاص بك للقيام بنفس الشيء (قفل / إلغاء قفل أي سمة شكل) باستخدام Aspose.Diagram for .NET.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Protection();

// Load diagram
Diagram diagram = new Diagram(dataDir + "ProtectAndUnprotect.vsd");
// Get page by name
Page page = diagram.Pages.GetPage("Flow 1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);

// Set protections
shape.Protection.LockAspect.Value = BOOL.True;
shape.Protection.LockBegin.Value = BOOL.True;
shape.Protection.LockCalcWH.Value = BOOL.True;
shape.Protection.LockCrop.Value = BOOL.True;
shape.Protection.LockCustProp.Value = BOOL.True;
shape.Protection.LockDelete.Value = BOOL.True;
shape.Protection.LockEnd.Value = BOOL.True;
shape.Protection.LockFormat.Value = BOOL.True;
shape.Protection.LockFromGroupFormat.Value = BOOL.True;
shape.Protection.LockGroup.Value = BOOL.True;
shape.Protection.LockHeight.Value = BOOL.True;
shape.Protection.LockMoveX.Value = BOOL.True;
shape.Protection.LockMoveY.Value = BOOL.True;
shape.Protection.LockRotate.Value = BOOL.True;
shape.Protection.LockSelect.Value = BOOL.True;
shape.Protection.LockTextEdit.Value = BOOL.True;
shape.Protection.LockThemeColors.Value = BOOL.True;
shape.Protection.LockThemeEffects.Value = BOOL.True;
shape.Protection.LockVtxEdit.Value = BOOL.True;
shape.Protection.LockWidth.Value = BOOL.True;
            
// Save diagram
diagram.Save(dataDir + "VisioShapeProtection_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
