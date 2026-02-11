---
title: العمل مع مصادر البيانات الخارجية
type: docs
weight: 200
url: /ar/net/working-with-external-data-sources/
description: يشرح هذا القسم كيفية العمل مع مصادر البيانات الخارجية مع Aspose.Diagram.
---
## **تحرير اتصال بيانات SQL Server وتحديث مجموعات السجلات**
Aspose.Diagram API يسمح للمستخدمين بتحرير اتصال بيانات SQL Server وتحديث كافة مجموعات السجلات. لإحضار البيانات إلى رسم Visio ، نحتاج إلى الوصول إلى بيانات SQL Server. تأكد من عدم فتح قاعدة البيانات في الوضع الخاص.
### **تحديث اتصال البيانات ومجموعات السجلات**
 من الظواهر الشائعة الآن ربط بيانات الرسوم التخطيطية Microsoft Visio من مصادر البيانات الخارجية. ال[جمع البيانات](http://www.aspose.com/api/net/diagram/aspose.diagram/dataconnectioncollection) فئة تحتوي على كافة اتصالات البيانات.
#### **عينة البرمجة**
يقوم الجزء التالي من التعليمات البرمجية بتحرير اتصال بيانات معين وكذلك تحديث جميع مجموعات السجلات المتاحة في Visio diagram.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_ExternalDataSources();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");
// Set connecting string
diagram.DataConnections[0].ConnectionString = "Data Source=MyServer;Initial Catalog=MyDB;Integrated Security=True";
// Set command
diagram.DataConnections[0].Command = "SELECT * from Project with(nolock)";
// Refresh all record sets
diagram.Refresh();
// Save Visio diagram
diagram.Save(dataDir + "EditDataConAndRefreshRecords_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

