---
title: إزالة حماية الشكل
type: docs
weight: 20
url: /ar/java/remove-shape-protection/
description: يوضح هذا القسم كيفية إزالة حماية الشكل باستخدام Aspose.Diagram.
---
## **إزالة الحماية للشكل Visio**
 تسمح حماية الأشكال Visio للمستخدمين بقفل جوانب معينة من الأشكال. تشمل جوانب الأشكال التي يمكن تأمينها من خلال حماية الشكل العرض والارتفاع وموضع x وموضع y والدوران والمزيد. يمكن للمطورين تحقيق ذلك باستخدام[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).
### **قم بتحرير حماية الشكل Visio**
**LockAspect**, **LockBegin**, **LockCalcWH**, **LockCrop**, **LockCustProp**, **قفل حذف**, **LockEnd**, **القفل**, **LockFromGroupFormat**, **لوكجروب**, **ارتفاع القفل**, **LockMoveX**, **LockMoveY**, **LockRotate**, **القفل**, **LockTextEdit**, **LockThemeColors**, **قفل التأثيرات**, **LockVtxEdit** و**عرض القفل** خصائص مكشوفة بواسطة[**حماية**](https://reference.aspose.com/diagram/java/com.aspose.diagram/protection) فئة دعم**Aspose.Diagram.BoolValue** هدف. يمكن استخدام هذه الخصائص لحماية الأشكال وإلغاء حمايتها.

في Microsoft Office Visio ، يمكن للمستخدم القيام بالإجراءات التالية لحماية أي شكل:

- افتح diagram في Microsoft Office Visio
- حدد أي شكل
- حدد "حماية" من قائمة "تنسيق" إذا كنت تستخدم Visio 2007 أو حدد "حماية" من قائمة "المطور" إذا كنت تستخدم Visio 2010
- في نافذة "الحماية" ، قم بإلغاء تحديد أي مربع نص لإلغاء تأمين أي سمة للشكل
- اضغط موافق'
### **قم بإزالة نموذج برمجة حماية الشكل**
استخدم الكود التالي في تطبيق Java الخاص بك للقيام بنفس الشيء (فتح أي سمة شكل) باستخدام Aspose.Diagram for Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VisioShapeProtection.class);
//Load diagram
Diagram diagram = new Diagram(dataDir + "ProtectAndUnprotect.vsd");
// get page by name
Page page = diagram.getPages().getPage("Flow 1");
// get shape by ID
Shape shape = page.getShapes().getShape(1);

// set protections
shape.getProtection().getLockAspect().setValue(BOOL.FALSE);
shape.getProtection().getLockBegin().setValue(BOOL.FALSE);
shape.getProtection().getLockCalcWH().setValue(BOOL.FALSE);
shape.getProtection().getLockCrop().setValue(BOOL.FALSE);
shape.getProtection().getLockCustProp().setValue(BOOL.FALSE);
shape.getProtection().getLockDelete().setValue(BOOL.FALSE);
shape.getProtection().getLockEnd().setValue(BOOL.FALSE);
shape.getProtection().getLockFormat().setValue(BOOL.FALSE);
shape.getProtection().getLockFromGroupFormat().setValue(BOOL.FALSE);
shape.getProtection().getLockGroup().setValue(BOOL.FALSE);
shape.getProtection().getLockHeight().setValue(BOOL.FALSE);
shape.getProtection().getLockMoveX().setValue(BOOL.FALSE);
shape.getProtection().getLockMoveY().setValue(BOOL.FALSE);
shape.getProtection().getLockRotate().setValue(BOOL.FALSE);
shape.getProtection().getLockSelect().setValue(BOOL.FALSE);
shape.getProtection().getLockTextEdit().setValue(BOOL.FALSE);
shape.getProtection().getLockThemeColors().setValue(BOOL.FALSE);
shape.getProtection().getLockThemeEffects().setValue(BOOL.FALSE);
shape.getProtection().getLockVtxEdit().setValue(BOOL.FALSE);
shape.getProtection().getLockWidth().setValue(BOOL.FALSE);
        
// save diagram
diagram.save(dataDir + "VisioShapeProtection_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

