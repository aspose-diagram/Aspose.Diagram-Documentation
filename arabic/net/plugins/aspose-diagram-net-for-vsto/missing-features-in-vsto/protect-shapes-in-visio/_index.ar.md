---
title: حماية الأشكال في Visio
type: docs
weight: 20
url: /ar/net/protect-shapes-in-visio/
---
LockAspect و LockBegin و LockCalcWH و LockCrop و LockCustProp و LockDelete و LockEnd و LockFormat و LockFromGroupFormat و LockGroup و LockHeight و LockMoveX و LockMoveY و LockRotate و LockSelect و LockTextEdit وخصائص LockThemeColors و LockTheme10 . يمكن استخدام هذه الخصائص لحماية / إلغاء حماية الأشكال.

في Visio ، تحتاج إلى القيام بالإجراءات التالية لحماية أي شكل:

- افتح diagram في MS Visio
- حدد أي شكل
- حدد "حماية ..." من قائمة "تنسيق" إذا كنت تستخدم Visio 2007 أو حدد "حماية" من قائمة "المطور" إذا كنت تستخدم Visio 2010
- في نافذة "الحماية" ، حدد / ألغِ تحديد أي مربع نص لقفل أو إلغاء قفل أي سمة للشكل
- اضغط موافق'

استخدم الكود التالي في تطبيق .NET الخاص بك للقيام بنفس الشيء (قفل أي سمة شكل) باستخدام Aspose.Diagram for .NET.

{{< highlight "csharp" >}}

 //Load diagram

Diagram diagram = new Diagram("ProtectShape.vsd");

Page page0 = diagram.Pages[0];

Shape shape = page0.Shapes[0];

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

diagram.Save("ProtectedShapesFile.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
## **تنزيل نموذج التعليمات البرمجية**
- [Bitbucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/src/master/Aspose.Diagram%20Vs%20VSTO%20Visio/)
