---
title: العمل مع الرؤوس والتذييلات
type: docs
weight: 150
url: /ar/java/working-with-headers-and-footers/
---
{{% alert color="primary" %}} 

يوفر Aspose.Diagram for Java آلية لإعداد الرؤوس والتذييلات للمخططات Microsoft Office Visio. يمكن للمطورين الحصول على سلسلة النص التي تظهر على الجانب الأيسر والأوسط والأيمن لرأس / تذييل المستند أو تعيينها. يمكنهم أيضًا تعيين هامش الرأس والتذييل مع خصائص خط النص.

{{% /alert %}} 
### **تعيين خصائص الرؤوس والتذييلات**
 ال[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)يقدم كائن الفئة خاصية HeaderFooter التي تسمح بالحصول على نص الرأس والتذييل والخط وقيم الهامش وتعيينهما. أثناء معاينة الطباعة للرسم Visio ، يمكن للمستخدمين النقر فوق زر الارتباط "تحرير الرأس والتذييل" في Microsoft Visio 2013 (في Microsoft Visio 2010 >> زر "Header & Footer"). هناك عدد قليل من الخيارات لإضافة نص كما هو موضح في لقطة الشاشة أدناه. يمكن للمستخدمين إدارة هذه الخصائص برمجيًا باستخدام Aspose.Diagram API على النحو التالي:

**إدارة نص الرؤوس والتذييلات والهوامش وخصائص الخط.** 

![ما يجب القيام به: image_بديل_نص](working-with-headers-and-footers_1.png)

يساعد الجزء التالي من التعليمات البرمجية في إدارة خصائص الرؤوس والتذييلات.
#### **عينات البرمجة**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ManageHeadersandFooters.class);
// call the diagram constructor to a load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// add page number at the right corner of header
diagram.getHeaderFooter().setHeaderRight("&p");

// set text at the center
diagram.getHeaderFooter().setHeaderCenter("Center of the header");

// set text at the left side
diagram.getHeaderFooter().setHeaderLeft("Left of the header");

// add text at the right corner of footer
diagram.getHeaderFooter().setFooterRight("Right of the footer");

// set text at the center
diagram.getHeaderFooter().setFooterCenter("Center of the footer");

// set text at the left side
diagram.getHeaderFooter().setFooterLeft("Left of the footer");

// set header & footer color
diagram.getHeaderFooter().setHeaderFooterColor(Color.getRed());

// set text font properties
diagram.getHeaderFooter().getHeaderFooterFont().setItalic(BOOL.TRUE);
diagram.getHeaderFooter().getHeaderFooterFont().setUnderline(BOOL.FALSE);

// save Visio diagram
diagram.save(dataDir + "EditConnectorGeometry_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
