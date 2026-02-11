---
title: العمل مع مصادر البيانات الخارجية
type: docs
weight: 190
url: /ar/java/working-with-external-data-sources/
---
## **تحديث اتصال البيانات للرسم Visio**
Aspose.Diagram API يسمح للمستخدمين بتحرير اتصال بيانات SQL Server للرسم Visio المرتبط. لإحضار البيانات إلى رسم Visio ، نحتاج إلى الوصول إلى بيانات SQL Server. تأكد من عدم فتح قاعدة البيانات في الوضع الخاص.

 من الظواهر الشائعة الآن ربط بيانات الرسوم التخطيطية Microsoft Visio من مصادر البيانات الخارجية. ال[جمع البيانات](https://reference.aspose.com/diagram/java/com.aspose.diagram/dataconnectioncollection) فئة تحتوي على كافة اتصالات البيانات.
### **عينة البرمجة**
يقوم الجزء التالي من التعليمات البرمجية بتحرير اتصال بيانات معين وكذلك تحديث جميع مجموعات السجلات المتاحة في Visio diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(EditDataConAndRefreshRecords.class);
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");
// set connecting string
diagram.getDataConnections().get(0).setConnectionString("Data Source=MyServer;Initial Catalog=MyDB;Integrated Security=True");
// set command
diagram.getDataConnections().get(0).setCommand("SELECT * from Project with(nolock)");
// save Visio diagram
diagram.save(dataDir + "EditDataConAndRefreshRecords_Out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

