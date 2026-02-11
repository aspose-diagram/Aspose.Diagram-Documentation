---
title: الترخيص
type: docs
weight: 60
url: /ar/java/licensing/
---
## **قيود إصدار التقييم**
 يمكن تنزيل نسخة تقييم مجانية من Aspose.Diagram for Java من[مستودع Aspose](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram).
### **التقييد**
يوفر الإصدار التقييمي جميع الميزات باستثناء ما يلي:

- يمكنك قراءة الأشكال العشرة الأولى فقط من الصفحة الأولى من ملف VSD الخاص بك.
- سترى أيضًا علامة مائية للتقييم في صور exoprted وملفات PDF.

 إذا كنت تريد تجربة Aspose.Diagram بدون قيود تقييم ، فاطلب ترخيصًا مؤقتًا لمدة 30 يومًا. يرجى الرجوع إلى[كيف تحصل على رخصة مؤقتة؟](https://purchase.aspose.com/temporary-license) للمزيد من المعلومات.
## **طلب ترخيص**
 يمكنك تنزيل إصدار تقييم من**Aspose.Diagram** for Java من[مستودع Aspose](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram). يوفر الإصدار التقييمي نفس الإمكانات تمامًا مثل الإصدار المرخص للمنتج. علاوة على ذلك ، يصبح الإصدار التقييمي مرخصًا ببساطة عند شراء ترخيص وإضافة سطرين من التعليمات البرمجية لتطبيق الترخيص.

 بمجرد أن تكون سعيدًا بتقييمك لـ**Aspose.Diagram** ، تستطيع[شراء رخصة](https://purchase.aspose.com/buy) على موقع الويب Aspose. تعرف على أنواع الاشتراكات المختلفة المعروضة. إذا كان لديك أي أسئلة ، فلا تتردد في الاتصال بفريق المبيعات Aspose.

يحمل كل ترخيص Aspose اشتراكًا لمدة عام واحد للترقيات المجانية لأي إصدارات جديدة أو إصلاحات تظهر خلال هذا الوقت. الدعم الفني مجاني وغير محدود ومقدم لكل من المستخدمين المرخصين والمقيّمين.

{{% alert color="primary" %}} 

 إذا كنت تريد الاختبار**Aspose.Diagram** بدون قيود الإصدار التقييمي ، اطلب ترخيصًا مؤقتًا لمدة 30 يومًا. يرجى الرجوع إلى[كيف تحصل على رخصة مؤقتة؟](https://purchase.aspose.com/temporary-license) للمزيد من المعلومات.

{{% /alert %}} 
### **تحديد الترخيص**
الترخيص عبارة عن ملف XML نص عادي يحتوي على تفاصيل مثل اسم المنتج وعدد المطورين المرخص لهم وتاريخ انتهاء الاشتراك وما إلى ذلك. الملف موقّع رقميًا ، لذا لا تقم بتعديل الملف ؛ حتى الإضافة غير المقصودة لكسر أسطر إضافي في الملف ستؤدي إلى إبطالها.

تحتاج إلى تطبيق ترخيص قبل إجراء أي عمليات مع المستندات. تأكد من القيام بذلك قبل إنشاء كائن Diagram. أنت مطالب فقط بتعيين ترخيص مرة واحدة لكل تطبيق أو عملية.

يمكن تحميل الترخيص من دفق أو ملف في المواقع التالية:

1. مسار صريح.
1. المجلد الذي يحتوي على Aspose.Diagram.jar.

 استخدم ال[License.setLicense ()](https://reference.aspose.com/diagram/java/com.aspose.diagram/License) طريقة لترخيص المكون. غالبًا ما تكون أسهل طريقة لتعيين ترخيص هي وضع ملف الترخيص في نفس المجلد مثل Aspose.Diagram.jar وتحديد اسم الملف فقط بدون مسار كما هو موضح في المثال التالي:
#### **مثال 1**
 في هذا المثال**Aspose.Diagram** سيحاول العثور على ملف الترخيص في المجلد الذي يحتوي على JARs للتطبيق الخاص بك.

**Java**

{{< highlight "csharp" >}}

 com.aspose.diagram.License license = new com.aspose.diagram.License();

license.setLicense("Aspose.Diagram.Java.lic");

{{< /highlight >}}
#### **مثال 2**
يقوم بتهيئة ترخيص من دفق.

**Java**

{{< highlight "csharp" >}}

 com.aspose.diagram.License license = new com.aspose.diagram.License();

license.setLicense(new java.io.FileInputStream("Aspose.Diagram.Java.lic"));

{{< /highlight >}}
### **التحقق من صحة الترخيص**
 من الممكن التحقق من صحة ما إذا تم تعيين الترخيص بشكل صحيح أم لا. ال[رخصة](https://reference.aspose.com/diagram/java/com.aspose.diagram/License)تحتوي الفئة على حقل isLicensed الذي سيعود صحيحًا إذا تم تعيين الترخيص بشكل صحيح.

**Java**

{{< highlight "csharp" >}}

 License license = new License();

license.setLicense("Aspose.Diagram.Java.lic");

if (License.isLicensed()) {

    System.out.println("License is Set!");

}

{{< /highlight >}}
## **تطبيق الترخيص المقنن**
Aspose.Diagram for Java API يسمح للمطورين بتطبيق الترخيص المقنن. إنها آلية ترخيص جديدة. سيتم استخدام آلية الترخيص الجديدة جنبًا إلى جنب مع طريقة الترخيص الحالية. يمكن للعملاء الذين يرغبون في دفع فواتيرهم بناءً على استخدام ميزات API استخدام الترخيص المقنن. لمزيد من التفاصيل ، يرجى الرجوع إلى[الأسئلة الشائعة حول الترخيص المقنن](https://purchase.aspose.com/faqs/licensing/metered)الجزء.

فئة جديدة[مقننة](https://reference.aspose.com/diagram/java/com.aspose.diagram/Metered) تمت إضافته لتطبيق المفتاح المقنن. يوضح مثال الرمز هذا كيفية تعيين المفاتيح العامة والخاصة التي تم قياسها:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// Initialize a Metered license class object
Metered metered = new Metered();
// apply public and private keys
metered.setMeteredKey("your-public-key", "your-private-key");
{{< /highlight >}}
```
