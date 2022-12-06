---
title: العمل مع الثيمات
type: docs
weight: 265
url: /ar/net/working-with-themes/
description: يشرح هذا القسم كيفية تطبيق سمة معدة مسبقًا على صفحة أو شكل باستخدام Aspose.Diagram.
---
## **كيفية تطبيق سمة محددة مسبقًا على صفحة أو شكل**
يمكن أن تكون هذه المقالة مفيدة لأي شخص يريد تعديل موضوع إعطاء VSDX باستخدام Aspose.Diagram. نستخدم ملف اختبار Themes1.vsdx ، انظر أدناه.

|**الموضوع 1.vsdx**|
|:- |
|![الموضوع 1.vsdx](theme1.png)|

### **قم بتطبيق نسق محدد مسبقًا على الصفحة**
تسمح واجهات API Aspose.Diagram بتطبيق نسق محدد مسبقًا للحصول على مظهر وأسلوب موحد للأشكال داخل الصفحة وعبر مستندات متعددة. قم بتنفيذ الخطوات التالية للقيام بذلك:

- قم بتكوين نسخة من فئة Diagram لتحميل diagram
- احصل على مثيل لفئة الصفحة لتعيين سمة
- قم بتعيين قيمة Preset لخاصية PresetTheme لمثيل الصفحة
#### **قم بتطبيق سمة محددة مسبقًا على نموذج لبرمجة الصفحة**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Theme-SetThemeForPage.cs" >}}

|**نتيجة تطبيق سمة محددة مسبقًا على صفحة**|
|:- |
|![SetTheme_out.vsdx](theme2.png)|

### **قم بتطبيق متغير نسق محدد مسبقًا على الصفحة**

تسمح واجهات API Aspose.Diagram بتطبيق متغير سمة مُعد مسبقًا للحصول على مظهر وشكل موحد للأشكال داخل الصفحة وعبر مستندات متعددة. قم بتنفيذ الخطوات التالية للقيام بذلك:

- قم بتكوين نسخة من فئة Diagram لتحميل diagram
- احصل على مثيل لفئة الصفحة لتعيين سمة
- قم بتعيين قيمة Preset لخاصية PresetTheme لمثيل الصفحة
- قم بتعيين قيمة PresetThemeVariant لمثيل الصفحة

#### **قم بتطبيق متغير نسق محدد مسبقًا على نموذج لبرمجة الصفحة**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Theme-SetThemeVariantForPage.cs" >}}

|**نتيجة تطبيق متغير نسق محدد مسبقًا على الصفحة**|
|:- |
|![SetTheme_out.vsdx](theme3.png)|

### **قم بتطبيق نسق محدد مسبقًا على شكل**

تسمح واجهات برمجة التطبيقات Aspose.Diagram بتطبيق نسق محدد مسبقًا على شكل داخل الصفحة. قم بتنفيذ الخطوات التالية للقيام بذلك:

- قم بتكوين نسخة من فئة Diagram لتحميل diagram
- احصل على مثيل لفئة الشكل لتعيين سمة
- قم بتعيين قيمة Preset لخاصية PresetTheme لمثيل Shape

#### **تطبيق سمة محددة مسبقًا على نموذج برمجة الشكل**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Theme-SetThemeForShape.cs" >}}

|**نتيجة تطبيق سمة محددة مسبقًا على شكل**|
|:- |
|![SetTheme_out.vsdx](theme4.png)|

### **تطبيق متغير نسق محدد مسبقًا على شكل**

تسمح واجهات برمجة التطبيقات Aspose.Diagram بتطبيق متغير نسق محدد مسبقًا على شكل داخل الصفحة. قم بتنفيذ الخطوات التالية للقيام بذلك:

- قم بتكوين نسخة من فئة Diagram لتحميل diagram
- احصل على مثيل لفئة الشكل لتعيين سمة
- قم بتعيين قيمة Preset لخاصية PresetTheme لمثيل Shape
- قم بتعيين قيمة PresetThemeVariant للخاصية PresetThemeVariant لمثيل الشكل

#### **تطبيق متغير سمة مُعد مسبقًا على عينة برمجة الشكل**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Theme-SetThemeVariantForShape.cs" >}}

|**نتيجة تطبيق متغير نسق محدد مسبقًا على شكل**|
|:- |
|![SetTheme_out.vsdx](theme5.png)|

### **قم بتطبيق Quickstyle متغير سمة مُعد مسبقًا على شكل**

Aspose.Diagram تسمح واجهات برمجة التطبيقات (API) بتطبيق نمط سريع للنسق المحدد مسبقًا على شكل داخل الصفحة. قم بتنفيذ الخطوات التالية للقيام بذلك:

- قم بتكوين نسخة من فئة Diagram لتحميل diagram
- احصل على مثيل لفئة الشكل لتعيين سمة
- قم بتعيين قيمة Preset لخاصية PresetTheme لمثيل Shape
- قم بتعيين قيمة PresetThemeVariant للخاصية PresetThemeVariant لمثيل الشكل
- قم بتعيين قيمة PresetThemeQuickStyle للخاصية PresetThemeQuickStyle لمثيل الشكل

#### **قم بتطبيق Quickstyle متغير سمة مُعد مسبقًا على عينة برمجة الشكل**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Theme-SetThemeQuickStyleForShape.cs" >}}

|**نتيجة تطبيق Quickstyle متغير سمة مُعد مسبقًا على شكل**|
|:- |
|![SetTheme_out.vsdx](theme6.png)|

### **تطبيق نمط سمة مُعد مسبقًا على شكل باستخدام طريقة SetPresetThemeStyleMatrics**

Aspose.Diagram تسمح واجهات برمجة التطبيقات (API) بتطبيق نمط سريع للنسق المحدد مسبقًا على شكل داخل الصفحة. قم بتنفيذ الخطوات التالية للقيام بذلك:

- قم بتكوين نسخة من فئة Diagram لتحميل diagram
- احصل على مثيل لفئة الشكل لتعيين سمة
- قم بتعيين قيمة Preset لخاصية PresetTheme لمثيل Shape
- قم بتعيين قيمة PresetThemeVariant للخاصية PresetThemeVariant لمثيل الشكل
- قم بتعيين نمط سمة عن طريق تعيين قيمة النمط وقيمة اللون لمثيل الشكل باستخدام طريقة SetPresetThemeStyleMatrics

#### **تطبيق نمط سمة مُعد مسبقًا على شكل باستخدام عينة برمجة أسلوب SetPresetThemeStyleMatrics**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Theme-SetThemeStyleMatricsForShape.cs" >}}

|**نتيجة تطبيق نمط سمة مُعد مسبقًا على شكل باستخدام طريقة SetPresetThemeStyleMatrics**|
|:- |
|![SetTheme_out.vsdx](theme7.png)|
