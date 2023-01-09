---
title: العمل مع الحماية
type: docs
weight: 90
url: /ar/java/working-with-protection/
---
## **مجموعة حماية Visio Diagram**
 تسمح حماية الرسوم التخطيطية للمستخدمين بقفل الخلفيات والماجستير (الإستنسل) والأشكال والأنماط بحيث لا يمكن تحريرها. يفيد ذلك في حماية أنماط الشركة ، على سبيل المثال ، وضمان الحصول على مظهر متناسق عبر مجموعة من الرسوم التخطيطية. يمكن للمطورين تحقيق ذلك باستخدام[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).
### **تحرير الحماية Visio Diagram**
 طرق getProtectBkgnds و getProtectMasters و getProtectShapes و getProtectStyles ، المكشوفة بواسطة[إعدادات المستند](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentSettings) فئة تدعم كائن com.aspose.diagram.BoolValue. يمكن استخدام هذه الخصائص لحماية الرسوم التخطيطية Microsoft Visio وإلغاء حمايتها.

في Microsoft Visio تقوم بحماية المستندات بهذه الطريقة:

1. افتح diagram في Microsoft Visio.
1. افتح نافذة مستكشف الرسم.
1.  انقر بزر الماوس الأيمن فوق diagram وحدد**حماية المستند** من القائمة.
1. في نافذة حماية المستند ، حدد الخيارات أو امسحها لقفل أو إلغاء قفل عناصر diagram مختلفة.
1.  انقر**نعم**.

**يرجى الاطلاع على كيف يمكننا التحقق من الخيارات أو مسحها يدويًا.** 

![ما يجب القيام به: image_بديل_نص](working-with-protection_1.png)

استخدم الكود أدناه في تطبيق Java لأداء نفس المهام - قفل وفتح عناصر مختلفة من diagram - باستخدام Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Protection-VisioDiagramProtection-VisioDiagramProtection.java" >}}
### **قم بتحرير حماية الشكل Visio**
 تسمح حماية الأشكال Visio للمستخدمين بقفل جوانب معينة من الأشكال. تشمل جوانب الأشكال التي يمكن تأمينها من خلال حماية الشكل العرض والارتفاع وموضع x وموضع y والدوران والمزيد. يمكن للمطورين تحقيق ذلك باستخدام[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

 ال**getLockAspect ()**, **getLockBegin ()**, **getLockCalcWH ()**, **getLockCrop ()**, **getLockCustProp ()**, **getLockDelete ()**, **getLockEnd ()**, **getLockFormat ()**, **getLockFromGroupFormat ()**, **getLockGroup ()**, **getLockHeight ()**, **getLockMoveX ()**, **getLockMoveY ()**, **getLockRotate ()**, **getLockSelect ()**, **getLockTextEdit ()**, **getLockThemeColors ()**, **getLockThemeEffects ()**, **getLockVtxEdit ()** و**getLockWidth ()** الطرق التي كشفها[حماية](https://reference.aspose.com/diagram/java/com.aspose.diagram/Protection) فئة تدعم كائن com.aspose.diagram.BoolValue. يمكن استخدام هذه الطرق لحماية / إلغاء حماية الأشكال.

في Visio ، تحتاج إلى القيام بالإجراءات التالية لحماية أي شكل:

1. افتح diagram في Microsoft Visio.
1. حدد شكلاً.
1.  يختار**حماية** من**شكل** القائمة (Visio 2007) ، أو حدد**حماية** من**مطور** القائمة (Visio 2010).
1.  في ال**حماية** نافذة ، حدد أو امسح خيارات لتأمين أو إلغاء قفل سمة الشكل ..
1.  انقر**نعم**.

**خيارات حماية الشكل ، كما هو موضح في Microsoft Visio** 

![ما يجب القيام به: image_بديل_نص](working-with-protection_2.png)

استخدم الكود التالي في تطبيق Java الخاص بك للقيام بنفس الشيء (قفل / إلغاء قفل أي سمة شكل) باستخدام Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Protection-VisioShapeProtection-VisioShapeProtection.java" >}}
