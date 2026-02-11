---
title: العمل مع النص
type: docs
weight: 120
url: /ar/java/working-with-text/
---
## **أدخل شكل نص في صفحة Visio**
 Aspose.Diagram API يتيح للمطورين إدراج شكل نص في أي مكان في صفحة Visio. لتحقيق ذلك ، فإن طريقة addText الخاصة بامتداد[صفحة](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) يأخذ الفصل معلمات PinX و PinY والعرض والارتفاع والنص.
### **أدخل نموذجًا لبرمجة شكل النص**
يضيف جزء الكود التالي شكل نص في Visio diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(InsertTextShape.class) + "Text/";
// create a new diagram
Diagram diagram = new Diagram();
// set parameters
double PinX = 1, PinY = 1, Width = 1, Height = 1;
String text = "Test text";
// add text to a Visio page
diagram.getPages().getPage(0).addText(PinX, PinY, Width, Height, text);
// save diagram 
diagram.save(dataDir + "InsertTextShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **تحديث Visio شكل النص**
 إلى جانب[إنشاء الرسوم البيانية](/diagram/ar/java/load-or-create-a-visio-drawing/)، Aspose.Diagram for Java يتيح لك العمل مع الأشكال بطرق مختلفة. تتناول هذه المقالة كيفية الوصول إلى النص في الأشكال وتحديثه.

 خاصية Text ، المكشوفة بواسطة ملف[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) فئة ، تدعم الكائن Aspose.Diagram.Text. يمكن استخدام الخاصية لاسترداد نص الشكل أو تحديثه.

**المدخلات diagram** 

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/6aEp7h0.png)

**Diagram بعد تغيير النص في الشكل المركزي من معالجة إلى نص جديد** 

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/o977cxw.png)

عملية تحديث نص الشكل مباشرة:

1. قم بتحميل diagram.
1. ابحث عن شكل معين.
1. قم بتعيين النص الجديد.
1. احفظ diagram.
### **تحديث نموذج برمجة نص الشكل**
يقوم الجزء التالي من التعليمات البرمجية بتحديث نص الشكل. يتم تحديد الأشكال من خلال معرفاتهم. تبحث مقاطع التعليمات البرمجية أدناه عن شكل يسمى العملية ومع المعرف 1 وتغيير نصه.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(UpdateShapeText.class); 
//Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "UpdateShapeText.vsd");
// get page by name
Page page = diagram.getPages().getPage("Flow 1");
//Find a particular shape and update its text
for (Shape shape :(Iterable<Shape>) page.getShapes())
{
    if (shape.getNameU().toLowerCase() == "process" && shape.getID() == 1)
    {
        shape.getText().getValue().clear();
        shape.getText().getValue().add(new Txt("New Text"));
    }
}
// save diagram
diagram.save(dataDir + "UpdateShapeText_Out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

## **قم بتطبيق ورقة أنماط مدمجة أو مخصصة على شكل Visio**
تخزن أوراق الأنماط Microsoft Visio معلومات التنسيق التي يمكن تطبيقها على الأشكال للحصول على مظهر وأسلوب عرض متسقين. Aspose.Diagram for Java يسمح لك بتطبيق أوراق الأنماط من داخل التطبيق.

 خصائص TextStyle و FillStyle و LineStyle المعروضة بواسطة ملف[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) فئة دعم[Aspose.Diagram.StyleSheet](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/stylesheet) هدف. يمكن استخدام الخاصية لاسترداد معلومات النمط وتطبيق أنماط مخصصة للنص والخط والتعبئة على diagram.

**المدخلات diagram** 

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/feV1x2N.png)

**diagram بعد تطبيق ورقة أنماط مخصصة تقوم بتعريف أنماط النص والخط والتعبئة** 

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/Xk9W0wN.png)
### **الأنماط المخصصة في Microsoft Visio**
لتطبيق أنماط مخصصة على الأشكال في Microsoft Visio:

1. افتح diagram في Microsoft Visio.
1.  يختار**تحديد الأنماط** من**شكل** القائمة (Visio 2007) ، أو انقر بزر الماوس الأيمن**الأنماط** في ال**مستكشف الرسم** نافذة ، وحدد**تحديد الأنماط** (Visio 2010).
1.  في ال**تحديد الأنماط** في مربع الحوار ، اكتب اسمًا جديدًا لورقة الأنماط المخصصة الخاصة بك. على سبيل المثال ، CustomStyle1.
1.  انقر على**نص**, **خط** و**يملأ** لتعيين أنماط النص والخط والتعبئة على التوالي.
1.  انقر**نعم**.

بعد تحديد أوراق الأنماط المخصصة في Microsoft Visio ، استخدم الكود التالي في تطبيق Java لتطبيق الأنماط المخصصة على الأشكال الخاصة بك. لاحظ أن نماذج التعليمات البرمجية أدناه تستدعي ورقة الأنماط المخصصة المحددة أعلاه: تحتاج إلى معرفة اسم وموقع الورقة التي تقوم بتطبيقها.

لتطبيق الأنماط المخصصة برمجيًا:

1. قم بتحميل diagram.
1. ابحث عن الشكل الذي تريد تطبيق النمط عليه.
1. قم بتحميل ورقة الأنماط.
1. تطبيق الأنماط.
1. احفظ diagram.
#### **تطبيق نموذج برمجة أنماط مخصصة**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ApplyCustomStyleSheets.class);

//Load diagram
Diagram diagram = new Diagram(dataDir + "ApplyCustomStyleSheets.vsd");
Shape sourceShape = null;
        
// get page by name
Page page = diagram.getPages().getPage("Flow 1");
//Find the shape that you want to apply style to
for (com.aspose.diagram.Shape shape : (Iterable<Shape>) page.getShapes())
{
    if (shape.getName() == "Process") {
        sourceShape = shape;
        break;
    }
}

StyleSheet customStyleSheet = null;

//Find the required style sheet
for (StyleSheet styleSheet : (Iterable<StyleSheet>) diagram.getStyleSheets())
{
    if (styleSheet.getName() == "CustomStyle1")
    {
        customStyleSheet = styleSheet;
        break;
    }
}

if (sourceShape != null && customStyleSheet != null)
{
    //Apply text style
    sourceShape.setTextStyle(customStyleSheet);
    //Apply fill style
    sourceShape.setFillStyle(customStyleSheet);
    //Apply line style
    sourceShape.setLineStyle(customStyleSheet);
}

 //Save the changed diagram as VDX
diagram.save(dataDir + "ApplyCustomStyleSheets_Out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

## **قم بتطبيق نمط مختلف على كل قيمة نصية لشكل**
 إلى جانب[إنشاء الرسوم البيانية](/diagram/ar/java/load-or-create-a-visio-drawing/)، Aspose.Diagram for Java يتيح لك العمل مع الأشكال بطرق مختلفة. تساعد هذه المقالة في إضافة قيم نصية متعددة إلى شكل وتطبيق نمط مختلف على كل قيمة نصية.

{{% alert color="primary" %}} 

يحتوي عنصر الشكل على عنصر يسمى Text ، والذي يحتوي على أحرف النص والعناصر الخاصة (cp و pp و tp و fld) التي تحدد نهاية تشغيل واحد وبداية تشغيل التالي. يحتوي Char Element على سمات التنسيق لنص الشكل ، مثل الخط واللون ونمط النص والحالة والموقع بالنسبة إلى الخط الأساسي وحجم النقطة.

{{% /alert %}} 
### **إضافة نص الشكل والأنماط**
**المدخلات diagram** 

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/ZqgQPQC.png)

**Diagram بعد إضافة قيم نصية مختلفة لشكل بنمط مختلف لكل قيمة نصية** 

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/7UWhFbU.png)
#### **إضافة نموذج برمجة نص وأنماط**
تضيف قطعة الكود التالية نصًا للشكل وأنماطًا مختلفة.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ApplyFontOnText.class);   
        
// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(1);
// clear shape text values and chars
shape.getText().getValue().clear();
shape.getChars().clear();

// mark character run and add text
shape.getText().getValue().add(new Cp(0));
shape.getText().getValue().add(new Txt("TextStyle_Regular\n"));
shape.getText().getValue().add(new Cp(1));
shape.getText().getValue().add(new Txt("TextStyle_Bold_Italic\n"));
shape.getText().getValue().add(new Cp(2));
shape.getText().getValue().add(new Txt("TextStyle_Underline_Italic\n"));
shape.getText().getValue().add(new Cp(3));
shape.getText().getValue().add(new Txt("TextStyle_Bold_Italic_Underline"));

// add formatting characters
shape.getChars().add(new Char());
shape.getChars().add(new Char());
shape.getChars().add(new Char());
shape.getChars().add(new Char());

//set properties e.g. color, font, size and style etc.
shape.getChars().get(0).setIX(0);
shape.getChars().get(0).getColor().setValue("#FF0000");
shape.getChars().get(0).getFont().setValue(1);
shape.getChars().get(0).getSize().setValue(0.22);
shape.getChars().get(0).getStyle().setValue(StyleValue.UNDEFINED);

//set properties e.g. color, font, size and style etc.
shape.getChars().get(1).setIX(1);
shape.getChars().get(1).getColor().setValue("#FF00FF");
shape.getChars().get(1).getFont().setValue(1);
shape.getChars().get(1).getSize().setValue(0.22);
shape.getChars().get(1).getStyle().setValue(StyleValue.BOLD | StyleValue.ITALIC);

//set properties e.g. color, font, size and style etc.
shape.getChars().get(2).setIX(2);
shape.getChars().get(2).getColor().setValue("#00FF00");
shape.getChars().get(2).getFont().setValue(1);
shape.getChars().get(2).getSize().setValue(0.22);
shape.getChars().get(2).getStyle().setValue(StyleValue.UNDERLINE | StyleValue.ITALIC);

//set properties e.g. color, font, size and style etc.
shape.getChars().get(3).setIX(3);
shape.getChars().get(3).getColor().setValue("#3333FF");
shape.getChars().get(3).getFont().setValue(1);
shape.getChars().get(3).getSize().setValue(0.22);
shape.getChars().get(3).getStyle().setValue(StyleValue.BOLD | StyleValue.ITALIC | StyleValue.UNDERLINE);
// save diagram
diagram.save(dataDir + "ApplyFontOnText_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **البحث عن نص الشكل واستبداله**
 ال[رسالة قصيرة](https://reference.aspose.com/diagram/java/com.aspose.diagram/txt) يسمح لك Class بتعديل نص الشكل. طريقة الاستبدال ، المكشوفة بواسطة[رسالة قصيرة](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/txt) فئة ، دعم تغيير نص الشكل.
تبحث أمثلة التعليمات البرمجية في هذه المقالة عن نص الشكل على الصفحة واستبداله.

**المدخلات diagram** 

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/lW5xaP0.png)


**diagram بعد تحرير الشكل** 

![ما يجب القيام به: image_بديل_نص](http://i.imgur.com/m33W1Tk.png)

عملية تغيير نص الشكل:

1. قم بتحميل diagram.
1. ابحث عن نص معين للشكل.
1. استبدل نص هذا الشكل
1. احفظ diagram.
### **بحث واستبدال عينة برمجة نصية**
توضح مقتطفات التعليمات البرمجية أدناه كيفية تعديل نص الشكل. تتكرر الشفرة عبر أشكال الصفحة.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(FindAndReplaceShapeText.class); 
// load diagram
Diagram diagram = new Diagram(dataDir + "FindReplaceText.vsdx");

DateFormat dateFormat = new SimpleDateFormat("dd/MMMM/yyyy");
Date myDate = new Date(System.currentTimeMillis());
Calendar cal = Calendar.getInstance();

// Prepare a collection old and new text
Hashtable<String, String> replacements = new Hashtable<String, String>();
replacements.put("[[CompanyName]]", "Research Society of XYZ");
replacements.put("[[CompanyName]]", "Research Society of XYZ");
replacements.put("[[EmplyeeName]]", "James Bond");
replacements.put("[[SubjectTitle]]", "The affect of the internet on social behavior in the industrialize world");

cal.setTime(myDate);
cal.add(Calendar.YEAR, -1);
System.out.println(dateFormat.format(cal.getTime()));
replacements.put("[[TimePeriod]]", dateFormat.format(cal.getTime()) + " -- " + dateFormat.format(myDate));

cal.setTime(myDate);
cal.add(Calendar.DAY_OF_MONTH, -7);
System.out.println(dateFormat.format(cal.getTime()));
replacements.put("[[SubmissionDate]]", dateFormat.format(cal.getTime()));
replacements.put("[[AmountReq]]", "$100,000");

cal.setTime(myDate);
cal.add(Calendar.DAY_OF_MONTH, 1);
System.out.println(dateFormat.format(cal.getTime()));
replacements.put("[[DateApproved]]", dateFormat.format(cal.getTime()));

// Iterate through the shapes of a page
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage("Page-1").getShapes())
{
    Set<String> keys = replacements.keySet();
    for(String key: keys)
    {
        for (FormatTxt txt : (Iterable<FormatTxt>) shape.getText().getValue())
        {
       	    Txt tx = (Txt)((txt instanceof Txt) ? txt : null);
            if (tx != null && tx.getText().contains(key))
            {
                //find and replace text of a shape
                tx.setText(tx.getText().replace(key, replacements.get(key)));
            }
        }
    }
}
// Save the diagram
diagram.save(dataDir + "FindAndReplaceShapeText_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **استخراج نص عادي من Visio Diagram صفحة**
Aspose.Diagram API يسمح للمطورين باستخراج نص عادي من صفحة Visio diagram. يمكنهم أيضًا تكرار الصفحات Visio diagram لتغطية النص Visio diagram بالكامل.

 Microsoft Office Visio يقوم باضافة النص الى الاشكال. ال[شكل](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) تحتوي الفئة على عنصر يسمى Text ، والذي يحتوي على أحرف النص والعناصر الخاصة (cp ، و pp ، و tp ، و fld) التي تحدد نهاية تشغيل واحد وبداية تشغيل ما يليه.
### **استخراج عينة برمجة نص عادي**
يتكرر جزء الكود التالي من خلال أشكال الصفحة Visio ويقوم بتصفية النص العادي بدون معلومات التنسيق.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
static String text = "";
public static void main(String[] args) throws Exception
{
       // The path to the documents directory.
       String dataDir = Utils.getDataDir(GetPlainTextOfVisio.class);
       // load diagram
       Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

       // get Visio diagram page
       Page page = diagram.getPages().getPage("Page-1");

       // iterate through the shapes
       for (Shape shape :(Iterable<Shape>) page.getShapes())
       {
           // extract plain text from the shape
           GetShapeText(shape);
       }
       // display extracted text
       System.out.println(text);
}
   private static void GetShapeText(Shape shape)
   {
   	// filter shape text
       if (shape.getText().getValue().getText() != "")
       	text += (shape.getText().getValue().getText().replaceAll("\\<.*?>",""));

       // for image shapes
       if (shape.getType() == TypeValue.FOREIGN)
           text += (shape.getName());

       // for group shapes
       if (shape.getType() == TypeValue.GROUP)
           for(Shape subshape : (Iterable<Shape>) shape.getShapes())
           {
               GetShapeText(subshape);
           }
   }

{{< /highlight >}}

