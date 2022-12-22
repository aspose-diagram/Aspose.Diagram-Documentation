---
title: أدخل صفحة فارغة جديدة في رسم Visio بلون الياقوت
type: docs
weight: 20
url: /ar/java/insert-a-new-blank-page-into-a-visio-drawing-in-ruby/
---
## **Aspose.Diagram - أدخل صفحة فارغة جديدة في رسم Visio**
 لإدراج صفحة فارغة جديدة في رسم Visio باستخدام**Aspose.Diagram Java لروبي** ، ببساطة استدعاء**إضافة صفحة** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود روبي**

{{< highlight "ruby" >}}

 تهيئة def ()

 بيانات_dir = File.dirname (File.dirname (File.dirname (File.dirname (__ملف__)))) + '/ بيانات /'

 اتصل بالمنشئ diagram لتحميل diagram من ملف VSD

 diagram = Rjb :: import ('com.aspose.diagram.Diagram'). new (data_dir + "Drawing.vsd")

 # احصل على معرف الصفحة القصوى

 الأعلى_صفحة_معرف = الحصول على_الأعلى_page_id (diagram)

 # تهيئة كائن صفحة جديد

 new_page = Rjb :: import ('com.aspose.diagram.Page'). new

 # اسم مجموعة

 new_page.setName ("صفحة جديدة")



 # تعيين معرف الصفحة

 الجديد_page.setID (ماكس_page_id + 1)

 # أو جرب منشئ الصفحة

 # صفحة newPage = صفحة جديدة (MaxPageId + 1) ؛

 # أضف صفحة فارغة جديدة

 diagram.getPages (). add (new_page)

 # احفظ diagram

 diagram.save (data_دير + "صفحة جديدة_الإخراج vdx "، Rjb :: import ('com.aspose.diagram.SaveFileFormat'). VDX)

 يضع "تمت إضافة صفحة جديدة".

نهاية

مواطنه الحصول على_الأعلى_page_id (diagram)

max = diagram.getPages (). getPage (0) .getID ()

 أنا = 1

 عندما أنا< diagram.getPages().getCount()

        if max < diagram.getPages().getPage(i).getID()

            max = diagram.getPages().getPage(i).getID()

        end

        i +=1

    end

    return max

end

{{< /highlight >}}
## **قم بتنزيل كود التشغيل**
 تحميل**أدخل صفحة فارغة جديدة في رسم Visio (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_Ruby/lib/asposediagramjava/Pages/addpage.rb)
