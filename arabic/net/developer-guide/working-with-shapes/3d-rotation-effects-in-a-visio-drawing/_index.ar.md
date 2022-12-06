---
title: تأثيرات الاستدارة ثلاثية الأبعاد في رسم Visio
type: docs
weight: 90
url: /ar/net/3d-rotation-effects-in-a-visio-drawing/
description: يوضح هذا القسم كيفية تعيين خصائص الاستدارة ثلاثية الأبعاد في ورقة الأشكال باستخدام Aspose.Diagram.
---
## **قم بتعيين خصائص الاستدارة ثلاثية الأبعاد في ورقة الأشكال**
Aspose.Diagram API يسمح للمطورين بتغيير قيم الدوران ثلاثي الأبعاد في ورقة الشكل. تتحكم قيم خلية RotationXAngle و RotationYAngle و RotationZAngle في درجة الدوران في كل من المحاور المعنية. تتحكم قيمة التعداد الخاصة بـ RotationType في نوع التدوير:

1. الدوران المتوازي ، حيث يتم تدوير الشكل دون احتساب المنظور الخطي.
1. تدوير المنظور ، حيث يتم تدوير الشكل بمنظور خطي.
1. الإعدادات المسبقة للدوران المائل (أسفل اليسار ، أسفل اليمين ، أعلى اليسار وأعلى اليمين) ، حيث يتم تدوير الشكل بإسقاط مائل.

 ال**KeepTextFlat** تشير قيمة الخلية إلى ما إذا كان نص الشكل سيتجاهل دوران الشكل ثلاثي الأبعاد. لا تنطبق على الدوران ثنائي الأبعاد. ال**مسافة من الأرض** تحدد قيمة الخلية المسافة التي يرفعها الكائن عن الأرض في النقاط عند تدويرها في 3-D. ال**إنطباع** تحدد قيمة الخلية زاوية المنظور لتدوير المنظور بالدرجات (من 0 إلى 359.9).
### **تعيين خصائص الاستدارة ثلاثية الأبعاد**
 تم الكشف عن عضو ThreeDFormat بواسطة[شكل](https://reference.aspose.com/diagram/net/aspose.diagram/shape)يمكن استخدام class لتعيين خصائص دوران ثلاثية الأبعاد.

يوضح الكود أدناه كيفية:

1. قم بتحميل رسم المصدر.
1. استرداد شكل عن طريق اسم الصفحة ومعلمات المعرف.
1. تعيين خصائص الاستدارة ثلاثية الأبعاد.
1. حفظ الرسم
#### **نموذج لبرمجة الدوران ثلاثي الأبعاد**
استخدم الكود التالي في تطبيق .NET الخاص بك لتعيين خصائص الاستدارة ثلاثية الأبعاد باستخدام Aspose.Diagram for .NET API.

**.NET, C#**

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram(@"c:\temp\TestTemplate.vsdx");

// get shape by ID and page name

Shape shape = diagram.Pages.GetPage("Page-1").Shapes.GetShape(0);



// set 3D rotation properties

shape.ThreeDFormat.RotationXAngle.Value = 2.61;

shape.ThreeDFormat.RotationYAngle.Value = 2.61;

shape.ThreeDFormat.RotationZAngle.Value = 3;

shape.ThreeDFormat.RotationType.Value = RotationTypeValue.ObliqueFromBottomLeft;

shape.ThreeDFormat.Perspective.Value = 0;

shape.ThreeDFormat.DistanceFromGround.Value = 0;

shape.ThreeDFormat.KeepTextFlat.Value = BOOL.True;

// save drawing

diagram.Save(@"c:\temp\TestTemplate.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
