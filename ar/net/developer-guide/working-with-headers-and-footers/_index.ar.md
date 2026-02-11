---
title: العمل مع الرؤوس والتذييلات
type: docs
weight: 140
url: /ar/net/working-with-headers-and-footers/
description: يشرح هذا القسم كيفية تعيين رؤوس وتذييلات Microsoft Office Visio مع Aspose.Diagram.
---
## **إدارة الرؤوس والتذييلات للمخططات Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) يوفر آلية لإعداد الرؤوس والتذييلات للمخططات Microsoft Office Visio. يمكن للمطورين الحصول على سلسلة النص التي تظهر على الجانب الأيسر والأوسط والأيمن لرأس / تذييل المستند أو تعيينها. يمكنهم أيضًا تعيين هامش الرأس والتذييل مع خصائص خط النص.
### **تعيين خصائص الرؤوس والتذييلات**
 ال[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)يقدم كائن الفئة خاصية HeaderFooter التي تسمح بالحصول على نص الرأس والتذييل والخط وقيم الهامش وتعيينهما. أثناء معاينة الطباعة للرسم Visio ، يمكن للمستخدمين النقر فوق زر الارتباط "تحرير الرأس والتذييل" في Microsoft Visio 2013 (في Microsoft Visio 2010 >> زر "Header & Footer"). هناك عدد قليل من الخيارات لإضافة نص كما هو موضح في لقطة الشاشة أدناه. يمكن للمستخدمين إدارة هذه الخصائص برمجيًا باستخدام Aspose.Diagram API على النحو التالي:
#### **عينة البرمجة**
يساعد الجزء التالي من التعليمات البرمجية في إدارة خصائص الرؤوس والتذييلات.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_HeadersAndFooters();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Add page number at the right corner of header
diagram.HeaderFooter.HeaderRight = "&p";

// Set text at the center
diagram.HeaderFooter.HeaderCenter = "Center of the header";

// Set text at the left side
diagram.HeaderFooter.HeaderLeft = "Left of the header";

// Add text at the right corner of footer
diagram.HeaderFooter.FooterRight = "Right of the footer";

// Set text at the center
diagram.HeaderFooter.FooterCenter = "Center of the footer";

// Set text at the left side
diagram.HeaderFooter.FooterLeft = "Left of the footer";

// Set header & footer color
diagram.HeaderFooter.HeaderFooterColor = Color.AliceBlue;

// Set text font properties
diagram.HeaderFooter.HeaderFooterFont.Italic = BOOL.True;
diagram.HeaderFooter.HeaderFooterFont.Underline = BOOL.False;

// Save Visio diagram
diagram.Save(dataDir + "ManageHeadersandFooters_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

