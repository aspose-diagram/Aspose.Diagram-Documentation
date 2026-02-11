---
title: الترخيص
type: docs
weight: 50
url: /ar/net/licensing/
description: Aspose. تدعو Diagram for .NET عملائها للحصول على رخصة كلاسيكية ورخصة عداد. بالإضافة إلى استخدام ترخيص محدود لاستكشاف المنتج بشكل أفضل.
---
## **أوجد Aspose.Diagram**
يمكنك بسهولة تنزيل Aspose.Diagram for .NET المنتج لأغراض التقييم. يرجى الرجوع إلى[Aspose.Diagram for .NET صفحة التحميل](https://www.nuget.org/packages/Aspose.Diagram/)لمعرفة أحدث إصدار. تنزيل التقييم مماثل للتنزيل الذي تم شراؤه. يصبح الإصدار التقييمي مرخصًا ببساطة عند إضافة بضعة أسطر من التعليمات البرمجية لتطبيق الترخيص.

يوفر إصدار التقييم Aspose.Diagram (بدون ترخيص محدد) وظائف المنتج الكاملة ، ولكنه يُدرج علامة مائية للتقييم في منتصف المستند عند الفتح والحفظ ، ويحد من قراءة الأشكال العشرة الأولى فقط من الصفحة الأولى من Visio diagram .

![ما يجب القيام به: image_بديل_نص](licensing_1.png)
### **قيود إصدار التقييم**
يوفر الإصدار التقييمي جميع الميزات باستثناء ما يلي:

- يمكنك قراءة أول عشرة أشكال فقط من الصفحة الأولى من Visio diagram.
- سترى أيضًا علامة مائية للتقييم في الصور المصدرة وملفات PDF.

{{% alert color="primary" %}} 

 إذا كنت تريد تجربة Aspose.Diagram بدون قيود تقييم ، فاطلب ترخيصًا مؤقتًا لمدة 30 يومًا. يرجى الرجوع إلى[كيف تحصل على رخصة مؤقتة؟](https://purchase.aspose.com/temporary-license) للمزيد من المعلومات.

{{% /alert %}} 
## **طلب ترخيص**
بمجرد أن تصبح سعيدًا بملف[تقييم](https://downloads.aspose.com/diagram/net) من Aspose.Diagram for .NET ، قم بشراء ترخيص على موقع الويب Aspose:[بوابة الشراء](https://purchase.aspose.com/buy) . تعرف على أنواع التراخيص المختلفة المتاحة. إذا كان لديك أية أسئلة،[اتصل بفريق المبيعات Aspose](https://about.aspose.com/contact) وسيسعدهم مساعدتك.

يحمل كل ترخيص Aspose اشتراكًا لمدة عام واحد للترقيات المجانية لأي إصدارات جديدة أو إصلاحات تظهر خلال هذا الوقت. نحن نقدم دعمًا فنيًا مجانيًا وغير محدود لكل من المستخدمين المرخصين والمستخدمين المقيّمين.

الترخيص عبارة عن ملف XML نص عادي يحتوي على تفاصيل مثل اسم المنتج وعدد المطورين المرخصين وتاريخ انتهاء الاشتراك وما إلى ذلك. الملف موقّع رقميًا ، لذا لا تقم بتعديل الملف: حتى إضافة فاصل أسطر إضافي إلى الملف يبطله.
### **متى يتم تطبيق الترخيص**
اتبع هذه القواعد البسيطة:

- يلزم تعيين الترخيص مرة واحدة فقط لكل مجال تطبيق.
- تحتاج إلى تعيين الترخيص قبل استخدام أي فئات Aspose.Diagram أخرى.
- لا يعد استدعاء SetLicense عدة مرات ضارًا ، ولكنه يضيع وقت المعالج.
- إذا كنت تقوم بتطوير Windows Forms أو تطبيق وحدة التحكم ، فاتصل بـ SetLicense في كود بدء التشغيل ، قبل استخدام فئات Aspose.Diagram.
- عند تطوير تطبيق ASP.NET ، قم باستدعاء SetLicense من الملف Global.asax.cs ، في أسلوب Aplication_Start المحمي. يتم استدعاؤه مرة واحدة عند بدء التطبيق.
- لا تستدعي SetLicense من داخل طرق Page_Load حيث أن ذلك يعني أن الترخيص سيتم تحميله في كل مرة يتم فيها تحميل صفحة ويب.
- إذا كنت تقوم بتطوير مكتبة فئة ، يمكنك استدعاء SetLicense من مُنشئ ثابت للفئة التي تستخدم Aspose.Diagram. يتم تنفيذ المُنشئ الثابت قبل إنشاء مثيل للفئة الخاصة بك مع التأكد من تعيين ترخيص Aspose.Diagram بشكل صحيح.
### **تطبيق الترخيص باستخدام ملف أو كائن دفق**
 استخدم ال[الترخيص](https://reference.aspose.com/diagram/net/aspose.diagram/license)طريقة لترخيص المكون. أسهل طريقة لتعيين ترخيص هي وضع ملف الترخيص في نفس المجلد مثل Aspose.Diagram.dll وتحديد اسم الملف ، بدون مسار ، كما هو موضح أدناه.
#### **تحميل ترخيص من ملف**
يقوم مقتطف الشفرة هذا بتهيئة ترخيص مخزن في ملف أو في مورد مضمن.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// Set path of the license file, i.e. c:\temp\
string dataDir = @"c:\temp\";

License license = new License();
license.SetLicense(dataDir + "Aspose.Diagram.lic");

{{< /highlight >}}

#### **تحميل ترخيص من كائن تيار**
تعمل مقتطفات التعليمات البرمجية هذه على تهيئة الترخيص من الدفق.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// Set path of the license file, i.e. c:\temp\
string dataDir = @"c:\temp\";
// Load an existing Visio file in the stream
FileStream LicStream = new FileStream(dataDir + "Aspose.Diagram.lic", FileMode.Open);

License license = new License();
license.SetLicense(LicStream);

{{< /highlight >}}

## **تطبيق الترخيص المقنن**
Aspose.Diagram for .NET API يسمح للمطورين بتطبيق الترخيص المقنن. إنها آلية ترخيص جديدة. سيتم استخدام آلية الترخيص الجديدة جنبًا إلى جنب مع طريقة الترخيص الحالية. يمكن للعملاء الذين يرغبون في دفع فواتيرهم بناءً على استخدام ميزات API استخدام الترخيص المقنن. لمزيد من التفاصيل ، يرجى الرجوع إلى[الأسئلة الشائعة حول الترخيص المقنن](https://purchase.aspose.com/faqs/licensing/metered)الجزء.

فئة جديدة[مقننة](https://reference.aspose.com/diagram/net/aspose.diagram/metered)تمت إضافته لتطبيق المفتاح المقنن. يوضح مثال الرمز هذا كيفية تعيين المفاتيح العامة والخاصة التي تم قياسها:


{{< highlight csharp >}}
// Initialize a Metered license class object
Aspose.Diagram.Metered metered = new Aspose.Diagram.Metered();
// apply public and private keys
metered.SetMeteredKey("your-public-key", "your-private-key");
{{< /highlight >}}

