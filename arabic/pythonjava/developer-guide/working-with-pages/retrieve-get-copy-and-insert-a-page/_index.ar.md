---
title: استرداد ، الحصول ، نسخ وإدراج صفحة
type: docs
weight: 10
url: /ar/python-java/retrieve-get-copy-and-insert-a-page/
---
## **استرجاع معلومات الصفحة**
في Microsoft Visio ، تكون الصفحات إما صفحات أمامية أو صفحات خلفية. للحصول على معلومات الصفحة ، على سبيل المثال معرف الصفحة واسم الصفحة ، حدد أولاً ما إذا كانت الصفحة هي خلفية أم صفحة مقدمة.

يمثل العنصر `Page` مساحة الرسم لصفحة أمامية أو صفحة خلفية. تدعم خاصية الصفحات المعروضة بواسطة الفئة `Diagram` مجموعة من كائنات الصفحة. يمكن استخدام هذه الخاصية لاسترداد معلومات الصفحة.

استخدم الخاصية `Page.Background` لتحديد ما إذا كانت الصفحة هي صفحة مقدمة أم خلفية.

### **استرداد نموذج برمجة معلومات الصفحة**
يسترد جزء الكود التالي معلومات الصفحات من diagram.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-RetrievePageInfo.py" >}}

## **احصل على Visio الصفحة من Diagram**
في بعض الأحيان ، يحتاج المطورون إلى الحصول على تفاصيل صفحة رسم Visio. يحتوي Aspose.Diagram لـ Python عبر Java على ميزات تساعدهم في القيام بذلك.

يقدم Aspose.Diagram لـ Python عبر Java فئة `Diagram` التي تمثل رسم Visio. تدعم خاصية الصفحات المعروضة بواسطة الفئة Diagram مجموعة من `Page` كائنات. تكشف فئة PageCollection عن طريقة `getPage` التي يمكن استدعاؤها للحصول على كائن الصفحة.

### **الحصول على عنصر صفحة Visio بواسطة المعرف**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. اتصل على Diagram.Pages class 'getPage method.

يوضح المثال التالي كيفية الحصول على كائن صفحة بواسطة معرف من رسم Visio.

#### **الحصول على كائن الصفحة عن طريق نموذج برمجة المعرف**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-GetVisioPagebyID.py" >}}

### **الحصول على Visio صفحة كائن حسب الاسم**
هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر للفئة Diagram.
1. استدعاء Diagram.Pages 'طريقة GetPage.

#### **الحصول على كائن الصفحة حسب نموذج برمجة الاسم**
يوضح المثال التالي كيفية الحصول على كائن صفحة بالاسم من رسم Visio.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-GetVisioPagebyName.py" >}}

## **نسخ صفحة Visio إلى Diagram آخر**
Aspose.Diagram لـ Python عبر Java API يسمح للمطورين بنسخ وإضافة محتوياته من Visio diagram إلى آخر. يشرح موضوع التعليمات هذا كيفية إنجاز هذه المهمة.

Aspose.Diagram لـ Python عبر Java API به فئة `Diagram` التي تمثل رسم Visio. تدعم خاصية الصفحات المعروضة بواسطة الفئة Diagram مجموعة من `Page` كائنات. تكشف فئة PageCollection عن طريقة `add` التي يمكن استدعاؤها لإضافة كائن صفحة آخر.

هذا المثال يعمل على النحو التالي:

1. قم بتكوين عنصر جديد للفئة Diagram.
1. قم بتحميل Visio diagram موجود في كائن الفئة Diagram.
1. أضف كافة الأساتذة من Visio diagram الذي تم تحميله
1. احصل على كائن الصفحة من diagram الذي تم تحميله (والذي يجب نسخه).
1. تعيين اسم كائن الصفحة والمعرف.
1. قم بإزالة الصفحة الفارغة من diagram الجديد (اختياري).
1. طريقة إضافة المكالمة لفئة PageCollection.
1. احفظ diagram الجديد في تخزين الكمبيوتر.

### **نسخ نموذج لبرمجة الصفحة Visio**
يوضح مثال الكود أدناه كيفية نسخ كائن صفحة Visio إلى رسم Visio آخر.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-CopyVisioPage.py" >}}

## **قم بنسخ Visio صفحة إلى نسخة صفحة أخرى**
تأخذ طريقة `copy` للفئة `Page` نسخة صفحة للنسخ.

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page()

# copy page

newPage.copy(diagram.getPages().getPage("Page-1"))

```

## **أدخل صفحة فارغة في رسم Visio**
Aspose.Diagram لـ Python عبر Java يمكن إدراج صفحة فارغة جديدة في الرسم Microsoft Office Visio. يصف هذا المثال الموضوع كيفية القيام بذلك.

تسمح طريقة `add` ، المعروضة بواسطة مجموعة الصفحات ، للمطورين بإضافة صفحة فارغة جديدة في Visio diagram. يجب تعيين معرف الصفحة.

### **أدخل نموذج برمجة صفحة فارغة**
يدخل جزء الكود التالي صفحة فارغة في رسم Visio:

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-InsertBlankPageInVisio.py" >}}

## **انقل موضع الصفحة في الرسم Visio**
يمكن لـ Aspose.Diagram لـ Python عبر Java API تحريك موضع الصفحة في الرسم Visio. تساعد طريقة `moveTo` ، التي تم الكشف عنها بواسطة فئة `Page` ، المطورين على تحريك موضع الصفحة.

### **نقل نموذج برمجة موضع الصفحة**
يأخذ عضو MoveTo فهرس الصفحة الهدف كمعامل لتحريك موضع الصفحة في الرسم Visio:

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page(1)

# move page in the diagram

newPage.moveTo(2)

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX)
```
