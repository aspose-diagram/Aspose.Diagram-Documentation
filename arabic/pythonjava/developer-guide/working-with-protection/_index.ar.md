---
title: العمل مع الحماية
type: docs
weight: 90
url: /ar/python-java/working-with-protection/
---
## **مجموعة حماية Visio Diagram**
تسمح حماية الرسوم التخطيطية للمستخدمين بقفل الخلفيات والماجستير (الإستنسل) والأشكال والأنماط بحيث لا يمكن تحريرها. يفيد ذلك في حماية أنماط الشركة ، على سبيل المثال ، وضمان الحصول على مظهر متناسق عبر مجموعة من الرسوم التخطيطية. يمكن للمطورين تحقيق ذلك باستخدام Aspose.Diagram لـ Python عبر Java.

### **تحرير الحماية Visio Diagram**
تدعم أساليب getProtectBkgnds و getProtectMasters و getProtectShapes و getProtectStyles ، المكشوفة بواسطة فئة DocumentSettings ، كائن BoolValue. يمكن استخدام هذه الخصائص لحماية الرسوم التخطيطية Microsoft Visio وإلغاء حمايتها.

في Microsoft Visio تقوم بحماية المستندات بهذه الطريقة:

1. افتح diagram في Microsoft Visio.
1. افتح نافذة مستكشف الرسم.
1.  انقر بزر الماوس الأيمن فوق diagram وحدد**حماية المستند** من القائمة.
1. في نافذة حماية المستند ، حدد الخيارات أو امسحها لقفل أو إلغاء قفل عناصر diagram مختلفة.
1.  انقر**نعم**.

**يرجى الاطلاع على كيف يمكننا التحقق من الخيارات أو مسحها يدويًا.** 

استخدم الكود أدناه في التطبيق الخاص بك لأداء نفس المهام - قفل وفتح عناصر مختلفة من diagram - باستخدام Aspose.Diagram لـ Python عبر Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-VisioDiagramProtection.py" >}}

### **قم بتحرير حماية الشكل Visio**
تسمح حماية الأشكال Visio للمستخدمين بقفل جوانب معينة من الأشكال. تشمل جوانب الأشكال التي يمكن تأمينها من خلال حماية الشكل العرض والارتفاع وموضع x وموضع y والدوران والمزيد. يمكن للمطورين تحقيق ذلك باستخدام Aspose.Diagram لـ Python عبر Java.

 ال**getLockAspect ()**, **getLockBegin ()**, **getLockCalcWH ()**, **getLockCrop ()**, **getLockCustProp ()**, **getLockDelete ()**, **getLockEnd ()**, **getLockFormat ()**, **getLockFromGroupFormat ()**, **getLockGroup ()**, **getLockHeight ()**, **getLockMoveX ()**, **getLockMoveY ()**, **getLockRotate ()**, **getLockSelect ()**, **getLockTextEdit ()**, **getLockThemeColors ()**, **getLockThemeEffects ()**, **getLockVtxEdit ()** و**getLockWidth ()** الطرق التي كشفها**حماية** فئة دعم كائن BoolValue. يمكن استخدام هذه الطرق لحماية / إلغاء حماية الأشكال.

في Visio ، تحتاج إلى القيام بالإجراءات التالية لحماية أي شكل:

1. افتح diagram في Microsoft Visio.
1. حدد شكلاً.
1.  يختار**حماية** من**شكل** القائمة (Visio 2007) ، أو حدد**حماية** من**مطور** القائمة (Visio 2010).
1.  في ال**حماية** نافذة ، حدد أو امسح خيارات لتأمين أو إلغاء قفل سمة الشكل ..
1.  انقر**نعم**.

**خيارات حماية الشكل ، كما هو موضح في Microsoft Visio** 

استخدم الكود التالي في تطبيق Java الخاص بك للقيام بنفس الشيء (قفل / فتح أي سمة شكل) باستخدام Aspose.Diagram لـ Python عبر Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-VisioShapeProtection.py" >}}
