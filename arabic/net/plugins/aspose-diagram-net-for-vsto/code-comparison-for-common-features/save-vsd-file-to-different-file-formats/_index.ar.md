---
title: احفظ VSD الملف إلى تنسيقات ملفات مختلفة
type: docs
weight: 10
url: /ar/net/save-vsd-file-to-different-file-formats/
---
في هذه المقالة ، نقارن ميزات التحويل لـ Aspose.Diagram for .NET مع VSTO. يحتوي على عينات كود .NET لتحويل ملفات VSD إلى تنسيقات ملفات VDX و PDF و JPEG.
## **VSTO**
يتيح لك VSTO البرمجة باستخدام ملفات Microsoft Visio. لحفظ ملف بتنسيقات أخرى:

1. قم بتكوين عنصر تطبيق Visio.
1. جعل كائن التطبيق غير مرئي.
1. قم بتحميل diagram.
1. احفظ في VDX و PDF و JPEG.
1. قم بإنهاء كائن التطبيق Visio.

{{< highlight "csharp" >}}

 //Create Visio Application Object

Visio.Application vsdApp = Application;

//Make Visio Application Invisible

vsdApp.Visible = false;

//Create a document object and load a diagram

Visio.Document vsdDoc = vsdApp.Documents.Open("Drawing.vsd");

//Save the VDX diagram

vsdDoc.SaveAs("Drawing1.vdx");

//Save as PDF file

vsdDoc.ExportAsFixedFormat(Visio.VisFixedFormatTypes.visFixedFormatPDF,

	"Drawing1.pdf", Visio.VisDocExIntent.visDocExIntentScreen,

	Visio.VisPrintOutRange.visPrintAll, 1, vsdDoc.Pages.Count, false, true,

	true, true, true, System.Reflection.Missing.Value);

Visio.Page vsdPage = vsdDoc.Pages[1];

//Save as JPEG Image

vsdPage.Export("Drawing1.jpg");

//Quit Visio Object

vsdApp.Quit();

{{< /highlight >}}
## **Aspose.Diagram**
عند البرمجة باستخدام Aspose.Diagram ، لا تحتاج إلى Microsoft Visio على الجهاز ، ويمكنك العمل بشكل مستقل عن Microsoft Office Automation. توضح مقتطفات التعليمات البرمجية أدناه كيفية:

1. قم بتحميل diagram.
1. احفظ diagram إلى VDX و PDF و JPEG.

{{< highlight "csharp" >}}

 //Load diagram

Diagram vsdDiagram = new Diagram("Drawing.vsd");

//Save the diagram as VDX

vsdDiagram.Save("Drawing1.vdx", SaveFileFormat.VDX);

//Save as PDF

vsdDiagram.Save("Drawing1.pdf", SaveFileFormat.PDF);

//Save as JPEG

vsdDiagram.Save("Drawing1.jpg", SaveFileFormat.JPEG);

{{< /highlight >}}
## **تنزيل نموذج التعليمات البرمجية**
- [جيثب](https://github.com/asposemarketplace/Aspose_for_VSTO/releases/download/Aspose.Diagram1.0/Save.VSD.file.to.different.file.formats.VDX.PDF.and.JPEG.Aspose.Diagram.zip)
- [سورس فورج](https://sourceforge.net/projects/asposevsto/files/Aspose.Diagram%20Vs%20VSTO%20Visio/Save%20VSD%20file%20to%20different%20file%20formats%20VDX%20PDF%20and%20JPEG%20\(Aspose.Diagram\).zip / تنزيل)
- [Bitbucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/downloads/Save%20VSD%20file%20to%20different%20file%20formats%20VDX%20PDF%20and%20JPEG%20\(Aspose.Diagram\).أَزِيز)
