---
title: إزالة حماية الشكل
type: docs
weight: 20
url: /ar/net/remove-shape-protection/
description: يشرح هذا القسم كيفية إزالة حماية الشكل.
---
## **إزالة الحماية للشكل Visio**
 تسمح حماية الأشكال Visio للمستخدمين بقفل جوانب معينة من الأشكال. تشمل جوانب الأشكال التي يمكن تأمينها من خلال حماية الشكل العرض والارتفاع وموضع x وموضع y والدوران والمزيد. يمكن للمطورين تحقيق ذلك باستخدام[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **قم بتحرير حماية الشكل Visio**
**LockAspect**, **LockBegin**, **LockCalcWH**, **LockCrop**, **LockCustProp**, **قفل حذف**, **LockEnd**, **القفل**, **LockFromGroupFormat**, **لوكجروب**, **ارتفاع القفل**, **LockMoveX**, **LockMoveY**, **LockRotate**, **القفل**, **LockTextEdit**, **LockThemeColors**, **قفل التأثيرات**, **LockVtxEdit** و**عرض القفل** خصائص مكشوفة بواسطة[**حماية**](http://www.aspose.com/api/net/diagram/aspose.diagram/Protection) فئة دعم**Aspose.Diagram.BoolValue** هدف. يمكن استخدام هذه الخصائص لحماية الأشكال وإلغاء حمايتها.

في Microsoft Office Visio ، يمكن للمستخدم القيام بالإجراءات التالية لحماية أي شكل:

- افتح diagram في Microsoft Office Visio
- حدد أي شكل
- حدد "حماية" من قائمة "تنسيق" إذا كنت تستخدم Visio 2007 أو حدد "حماية" من قائمة "المطور" إذا كنت تستخدم Visio 2010
- في نافذة "الحماية" ، قم بإلغاء تحديد أي مربع نص لإلغاء تأمين أي سمة للشكل
- اضغط موافق'
### **قم بإزالة نموذج برمجة حماية الشكل**
استخدم الكود التالي في تطبيق .NET الخاص بك للقيام بنفس الشيء (فتح أي سمة شكل) باستخدام Aspose.Diagram for .NET.

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
shape.Protection.LockAspect.Value = BOOL.False;
shape.Protection.LockBegin.Value = BOOL.False;
shape.Protection.LockCalcWH.Value = BOOL.False;
shape.Protection.LockCrop.Value = BOOL.False;
shape.Protection.LockCustProp.Value = BOOL.False;
shape.Protection.LockDelete.Value = BOOL.False;
shape.Protection.LockEnd.Value = BOOL.False;
shape.Protection.LockFormat.Value = BOOL.False;
shape.Protection.LockFromGroupFormat.Value = BOOL.False;
shape.Protection.LockGroup.Value = BOOL.False;
shape.Protection.LockHeight.Value = BOOL.False;
shape.Protection.LockMoveX.Value = BOOL.False;
shape.Protection.LockMoveY.Value = BOOL.False;
shape.Protection.LockRotate.Value = BOOL.False;
shape.Protection.LockSelect.Value = BOOL.False;
shape.Protection.LockTextEdit.Value = BOOL.False;
shape.Protection.LockThemeColors.Value = BOOL.False;
shape.Protection.LockThemeEffects.Value = BOOL.False;
shape.Protection.LockVtxEdit.Value = BOOL.False;
shape.Protection.LockWidth.Value = BOOL.False;
            
// Save diagram
diagram.Save(dataDir + "RemoveShapeProtection_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
