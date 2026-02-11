---
title: العمل مع عناصر النافذة
type: docs
weight: 100
url: /ar/net/working-with-window-elements/
description: يوضح هذا القسم الحصول على خاصية عناصر النافذة في visio مع Aspose.Diagram.
---
## **استرجع عناصر النافذة من رسم Visio**
 يمكن أن تحتوي نافذة التطبيق Visio الرئيسية على أي ملفات Visio مفتوحة ، مثل متصفحات الويب الحديثة التي تسمح بعدة صفحات ويب مبوبة في نافذة واحدة. يمكن للمطورين استرداد كائنات Window باستخدام[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

 ال[نافذة جمع](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection) يمثل الكائن قائمة[نافذة او شباك](http://www.aspose.com/api/net/diagram/aspose.diagram/window)الكائنات المتوفرة في الرسم. تدعم خاصية Windows ، المعروضة بواسطة الفئة Diagram ، مجموعة من كائنات Aspose.Diagram.Window. يمكن استخدام هذه الخاصية لاسترداد معلومات النافذة أي معرف النافذة والنوع والارتفاع والعرض والحالة.
### **استرجاع نموذج برمجة عناصر النافذة**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Iterate through the window elements
foreach (Window window in diagram.Windows)
{
    Console.WriteLine("ID: " + window.ID);
    Console.WriteLine("Type: " + window.WindowType);
    Console.WriteLine("Window height: " + window.WindowHeight);
    Console.WriteLine("Window width: " + window.WindowWidth);
    Console.WriteLine("Window state: " + window.WindowState);
}

{{< /highlight >}}

## **أضف عنصر النافذة إلى Visio Diagram**
 يمكن أن تحتوي نافذة التطبيق Visio الرئيسية على أي ملفات Visio مفتوحة ، مثل متصفحات الويب الحديثة التي تسمح بعدة صفحات ويب مبوبة في نافذة واحدة. يمكن للمطورين الآن إضافة كائن Window جديد في مثيل Microsoft Visio باستخدام[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).

 ال[نافذة او شباك](http://www.aspose.com/api/net/diagram/aspose.diagram/window) يمثل الكائن نافذة مفتوحة في مثيل Microsoft Visio. ال[يضيف](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection/methods/add) الطريقة التي يتعرض لها[نافذة جمع](http://www.aspose.com/api/net/diagram/aspose.diagram/windowcollection) class ، تسمح بإضافة كائن Window جديد.
### **إضافة نموذج برمجة عنصر النافذة**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Initialize window object
Window window = new Window();
// Set window state
window.WindowState = WindowStateValue.Maximized;
// Set window height
window.WindowHeight = 500;
// Set window width
window.WindowWidth = 500;
// Set window type
window.WindowType = WindowTypeValue.Stencil;
// Add window object
diagram.Windows.Add(window);

// Save in any supported format
diagram.Save(dataDir + "AddWindowElementInVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **أضف دعمًا للشبكات الديناميكية ونقاط الاتصال**
تساعدك الشبكة الديناميكية على وضع الأشكال الجديدة رأسياً وأفقياً بالنسبة للأشكال التي وضعتها بالفعل في الرسم. فيما يتعلق بنقاط الاتصال ، بمجرد تمييزها على أنها محددة ، ستساعدنا في رؤية نقاط الاتصال عندما نكون في طور الاتصال بها. يمكننا تحقيق كلا الخيارين باستخدام[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).
### **دعم الشبكات الديناميكية ونقاط الاتصال في رسومات Visio**
 ال[نافذة او شباك](http://www.aspose.com/api/net/diagram/aspose.diagram/window) تقدم الفئة خصائص DynamicGridEnabled و ShowConnectionPoints. يمكن استخدام هذه الخصائص لتطبيق الإعدادات لدعم الشبكات الديناميكية وإظهار خيارات نقاط الاتصال.
#### **إضافة نموذج برمجة الدعم**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get window object by index
Window window = diagram.Windows[0];
// Check dynamic grid option
window.DynamicGridEnabled = BOOL.True;
// Check connection points option
window.ShowConnectionPoints = BOOL.True;
            
// Save visio drawing
diagram.Save(dataDir + "AddSupportOfVisualAids_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **إظهار وإخفاء الشبكات والمساطر والأدلة وفواصل الصفحات من Visio Diagram**
 Microsoft Office Visio له زوج من المساطر وشبكة ونوعين من الأدلة وعلم فواصل الصفحات لمعرفة ما سيتم طباعته على كل صفحة. يمكن للمطورين تطبيق هذه الإعدادات باستخدام[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/)يتم تطبيق الإعدادات بشكل عام على صفحة واحدة.

 ال[نافذة او شباك](http://www.aspose.com/api/net/diagram/aspose.diagram/window)تقدم الفئة خصائص ShowGrid و ShowGuides و ShowRulers و ShowPageBreaks. يمكن استخدام هذه الخصائص لتطبيق الإعدادات لإظهار وإخفاء الشبكات والأدلة والمساطر وفواصل الصفحات.
### **عينة البرمجة**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_WindowElements();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get window object by index
Window window = diagram.Windows[0];
// Set visibility of grid
window.ShowGrid = BOOL.True;
// Set visibility of guides
window.ShowGuides = BOOL.True;
// Set visibility of rulers
window.ShowRulers = BOOL.True;
// Set visibility of page breaks
window.ShowPageBreaks = BOOL.True;

// Save diagram
diagram.Save(dataDir + "DisplayGridsRulersGuidesAndPageBreaks_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

