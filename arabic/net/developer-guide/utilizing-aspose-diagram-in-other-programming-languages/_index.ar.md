---
title: استخدام Aspose.Diagram في لغات البرمجة الأخرى
type: docs
weight: 120
url: /ar/net/utilizing-aspose-diagram-in-other-programming-languages/
description: توضح هذه الصفحة كيفية استخدام Aspose.Diagram في لغات البرمجة الأخرى.
---
## **استخدم Aspose.Diagram for .NET عبر COM Interop**
 تنطبق المعلومات الواردة في هذا الموضوع على السيناريوهات التي يطلب المطورون استخدامها[Aspose.Diagram for .NET](/diagram/ar/net/home/) عبر COM Interop بأي لغة مدعومة.
### **العمل مع COM Interop**
يتم تنفيذ Aspose.Diagram for .NET تحت سيطرة .NET Framework ويسمى هذا الرمز المدار. الكود المكتوب بجميع اللغات التي تعمل خارج .NET Framework ويسمى رمز غير مُدار. يحدث التفاعل بين الكود غير المُدار و Aspose.Diagram عبر منشأة .NET تسمى COM Interop.

كائنات Aspose.Diagram هي .NET كائنات ، ولكن عند استخدامها عبر COM Interop ، فإنها تظهر ككائنات COM في لغة البرمجة الخاصة بك. لذلك ، من الأفضل التأكد من معرفة كيفية إنشاء واستخدام كائنات COM في لغة البرمجة الخاصة بك ، قبل البدء في استخدام[Aspose.Diagram for .NET](/diagram/ar/net/home/).

- في عالم COM ، نميز خادم COM وعميل COM. قام خادم COM بتخزين فئات COM بينما يطلب عميل COM خادم COM لمثيلات الفئات ، أي كائنات COM.
-  يمكن لعميل COM أو تطبيق العميل ببساطة معرفة محتويات فئة COM أو أن يكون غير مدرك تمامًا لأساليبها وخصائصها. لذلك يمكن لتطبيق العميل اكتشاف بنية فئة COM عند التجميع / البناء أو أثناء التنفيذ فقط. تُعرف عملية "الاكتشاف" بالربط ولذا لدينا**الربط المبكر** و**الربط المتأخر**.
- باختصار ، تشبه فئة COM الصندوق الأسود ، وهناك حاجة إلى استخدام مكتبة النوع ، ويحتوي هذا الملف الثنائي على وصف لطرق فئة COM وخصائصها وأي لغة عالية المستوى تدعم العمل مع كائنات COM غالبًا ما تحتوي على تعبير نحوي لإضافة مكتبة كتابة ، من أجل المثال هذا[**#يستورد**](http://msdn.microsoft.com/en-us/library/8etzzkb6.aspx) في C++.
- تُستخدم مكتبة النوع للربط المبكر.
-  يمكن أن يكشف كائن COM عن طرقه وخصائصه بطريقتين: عن طريق a**واجهة الإرسال** (dispinterface) وفيها**vtable** (جدول الوظيفة الافتراضية).
-  في حدود**صرف** ، يتم تحديد كل طريقة وممتلكات بواسطة عضو فريد ؛ هذا العضو هو معرّف إرسال الوظيفة (أو**ديسيد**).
- **vtable** هي مجرد مجموعة من المؤشرات للوظائف التي تدعمها واجهة فئة COM.
-  الكائن الذي يعرض طرقه من خلال كلا الواجهتين يدعم a**واجهة مزدوجة**.
- هناك مزايا لكلا النوعين من الربط. يوفر لك الربط المبكر أداءً متزايدًا وفحصًا لصيغة وقت الترجمة. يعد الربط المتأخر أكثر فائدة عندما تكتب عملاء تنوي أن تكون***متوافق مع الإصدارات المستقبلية*** من فئة COM الخاصة بك. مع الربط المتأخر ، لا تكون المعلومات من مكتبة النوع "مترابطة" في عميلك ، لذلك يمكنك أن تثق بدرجة أكبر في أن عميلك يمكنه العمل مع الإصدارات المستقبلية من فئة COM بدون تغييرات في التعليمات البرمجية.
-  تتميز آلية الربط المتأخرة بميزة كبيرة: إذا قرر منشئ مكتبة الارتباط الديناميكي COM إصدار إصدار جديد ، بتخطيط واجهة وظيفة مختلف ، فلن يتعطل أي رمز يستدعي هذه الأساليب ما لم تعد الأساليب متاحة ؛ حتى لو**vtable**هو الربط المتأخر المختلف الذي يدير اكتشاف DISPIDs الجديدة واستدعاء الطرق المناسبة.

 فيما يلي الموضوعات التي ستحتاج في النهاية إلى إتقانها:

- استخدام كائنات COM في لغة البرمجة الخاصة بك. راجع وثائق لغة البرمجة الخاصة بك والمواضيع الخاصة باللغة بشكل أكبر في هذا التوثيق.
-  العمل مع كائنات COM المكشوفة بواسطة .NET COM Interop. نرى[التعامل مع التعليمات البرمجية غير المُدارة](https://docs.microsoft.com/en-us/dotnet/framework/interop/) و[تعريض .NET Framework مكونات إلى COM](https://docs.microsoft.com/en-us/dotnet/framework/interop/exposing-dotnet-components-to-com) في MSDN.
-  Aspose.Diagram نموذج عنصر الوثيقة. نرى[Aspose.Diagram دليل المبرمج](https://docs.aspose.com/diagram/net/developer-guide/) و[API المرجع](https://reference.aspose.com/diagram/net).
#### **قم بتسجيل Aspose.Diagram for .NET مع COM Interop**
تحتاج إلى تثبيت Aspose.Diagram for .NET والتأكد من تسجيله في COM Interop (مع ضمان إمكانية استدعاؤه من رمز غير مُدار).

لتسجيل Aspose.Diagram for .NET لـ COM Interop يدويًا:

1.  من**بداية** القائمة ، حدد**كل البرامج** ، ومن بعد**Microsoft Visual Studio**, **أدوات Visual Studio** وأخيرا**موجه أوامر Visual Studio**. في بعض أنظمة التشغيل ، يتوفر أيضًا في الموقع: "C: \ Program Files (x86) \ Microsoft SDKs \ Windows \ v7.0A \ bin \ x64"
1.  أدخل الأمر لتسجيل التجمع:
   1. .NET Framework 2.0
regasm "C: \ Program Files \ Aspose \ Aspose.Diagram for .NET \ bin \ net2.0 \ Aspose.Diagram.dll" / codebase
   1. .NET Framework 3.5
 regasm "C: \ Program Files \ Aspose \ Aspose.Diagram for .NET \ bin \ net3.5 \ Aspose.Diagram.dll" / codebase
   1. .NET Framework 4.0
 regasm "C: \ Program Files \ Aspose \ Aspose.Diagram for .NET \ bin \ net4.0 \ Aspose.Diagram.dll" / codebase

{{% alert color="primary" %}} 

انتبه إلى أن / codebase ضروري فقط إذا لم يكن Aspose.Diagram.dll موجودًا في GAC ، فإن استخدام هذا الخيار يجعل مسار وضع Regasm للتجميع في التسجيل.

{{% /alert %}} {{% alert color="primary" %}} 

 regasm.exe أداة مضمنة في .NET Framework SDK. توجد جميع أدوات SDK .NET Framework في*\ Microsoft .NET \ Framevork \ <FrameworkVersion>* الدليل ، على سبيل المثال*ج: \ Windows \ Microsoft .NET \ Framework \ v4.0.30319*. إذا كنت تستخدم Visual Studio .NET:
 من**بداية** القائمة ، حدد**البرامج** ، تليها**Microsoft Visual Studio .NET** ، ومن بعد**أدوات Visual Studio .NET** وأخيرا**موجه الأوامر المرئي .NET 2003**.
يقوم بتشغيل موجه الأوامر مع مجموعة متغيرات البيئة الضرورية.

{{% /alert %}} 
##### **ProgIDs**
ProgID تعني "المعرف البرمجي". إنه اسم فئة COM التي تستخدم لإنشاء كائن. تتكون ProgIDs من اسم المكتبة "Aspose.Diagram" واسم الفئة.
##### **اكتب مكتبة**
إذا كانت لغة البرمجة الخاصة بك (على سبيل المثال Visual Basic أو Delphi) تسمح لك بالرجوع إلى مكتبة نوع COM ، فقم بإضافة مرجع إلى Aspose.Diagram.tlb ولرؤية جميع فئات Aspose.Diagram for .NET وطرقها وخصائصها والتعدادات في مستعرض الكائنات الخاص بك.

لإنشاء ملف TLB:

- .NET Framework 2.0
 regasm "C: \ Program Files \ Aspose \ Aspose.Diagram for .NET \ bin \ net2.0 \ Aspose.Diagram.dll" / tlb: "C: \ Program Files \ Aspose \ Aspose.Diagram for .NET \ bin \ net2.0 \ Aspose.Diagram.t" / codebase
- .NET Framework 3.5
 regasm "C: \ Program Files \ Aspose \ Aspose.Diagram for .NET \ bin \ net3.5 \ Aspose.Diagram.dll" / tlb: "C: \ Program Files \ Aspose \ Aspose.Diagram for .NET \ bin \ net3.5 \ Aspose.Diagram.t" / codebase
- .NET Framework 4.0
regasm "C: \ Program Files \ Aspose \ Aspose.Diagram for .NET \ bin \ net4.0 \ Aspose.Diagram.dll" / tlb: "C: \ Program Files \ Aspose \ Aspose.Diagram for .NET \ bin \ net4.0 \ Aspose.Diagram.t" / codebase
#### **إنشاء كائنات COM**
يشبه إنشاء كائن COM إنشاء كائن .NET عادي. بمجرد الإنشاء ، يمكنك الوصول إلى أساليب الكائن وخصائصه ، كما لو كان كائن COM.

تحتوي بعض الطرق على حمولات زائدة وسيتم عرضها بواسطة COM Interop مع إضافة لاحقة رقمية إليها ، باستثناء الطريقة الأولى التي تظل بدون تغيير. على سبيل المثال ، تصبح الأحمال الزائدة لطريقة الحفظ Diagram Diagram.Save و Diagram.Save_2 وهكذا.

{{% alert color="primary" %}} 

 لمزيد من المعلومات ، راجع المقالات الخاصة بلغة معينة في هذه الوثائق.

{{% /alert %}} 
## **Aspose.Diagram الموارد**
فيما يلي روابط لبعض الموارد المفيدة التي قد تحتاجها لإنجاز مهامك.
- [Aspose.Diagram for Java التوثيق عبر الإنترنت](https://docs.aspose.com/diagram/java/)
- [Aspose.Diagram لـ Node.js عبر التوثيق عبر الإنترنت Java](https://docs.aspose.com/diagram/nodejsjava/)
- [Aspose.Diagram لـ Python عبر Java التوثيق عبر الإنترنت](https://docs.aspose.com/diagram/pythonjava/)

##### **إنشاء مجموعة غلاف**
إذا كنت بحاجة إلى استخدام العديد من فئات وطرق وخصائص Aspose.Diagram for .NET ، ففكر في إنشاء مجموعة مجمعة (باستخدام C# أو أي لغة برمجة .NET أخرى). تساعد تجميعات الغلاف على تجنب استخدام Aspose.Diagram for .NET مباشرةً من التعليمات البرمجية غير المُدارة.

تتمثل إحدى الطرق الجيدة في تطوير مجموعة .NET تشير إلى Aspose.Diagram for .NET وتقوم بكل العمل معها ، ولا تعرض سوى مجموعة قليلة من الفئات والطرق للتعليمات البرمجية غير المُدارة. يجب أن يعمل التطبيق الخاص بك مع مكتبة الغلاف الخاصة بك فقط.

 يؤدي تقليل عدد الفئات والطرق التي تحتاج إلى استدعاؤها عبر COM Interop إلى تبسيط المشروع. غالبًا ما يتطلب استخدام فئات .NET عبر COM Interop مهارات متقدمة.
## **قم بإنشاء رسم Visio فارغ في PHP باستخدام COM Interop**
### **المتطلبات الأساسية**
 قم بتكوين PHP الخاص بك للعمل مع COM. نرى<http://www.php.net/manual/en/ref.com.php> . لمزيد من المعلومات ، يرجى مراجعة المقالة المسماة[استخدم Aspose.Diagram for .NET عبر COM Interop](/diagram/ar/net/home/).
### **تكوين رسم Visio فارغ**
 هذا تطبيق بسيط يوضح لك كيفية إنشاء رسم Visio فارغ باستخدام[Aspose.Diagram for .NET](/diagram/ar/net/home/) في PHP عبر COM Interop.

**بي أتش بي**

{{< highlight "csharp" >}}

 <?php

echo "<h3>Calling Aspose.Diagram for .NET from PHP using COM Interoperatibility</h3>";

//set license

$lic = new COM("Aspose.Diagram.License");

$lic->SetLicense("D:\ASPOSE\Licences\Aspose.Total licenses\Aspose.Total.lic");

// create a new instance of Diagram object using COM interop

$diagram = new COM("Aspose.Diagram.Diagram");

// Save the Visio drawing in the VDX format

$diagram->Save("d:\diagramtest\MyOutput.vdx", 0);

?>



{{< /highlight >}}
