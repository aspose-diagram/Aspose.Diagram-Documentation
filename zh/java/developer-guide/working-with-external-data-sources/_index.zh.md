---
title: 使用外部数据源
type: docs
weight: 190
url: /zh/java/working-with-external-data-sources/
---
## **更新 Visio 图形的数据连接**
Aspose.Diagram API 允许用户编辑链接的 Visio 图形的 SQL Server 数据连接。要将数据引入 Visio 绘图，我们需要访问 SQL Server 数据。确保数据库未以独占模式打开。

从外部数据源链接Microsoft Visio图表的数据现在是一种普遍现象。这[数据连接集合](https://reference.aspose.com/diagram/java/com.aspose.diagram/dataconnectioncollection)类包含所有数据连接。
### **编程范例**
下面的一段代码编辑一个特定的数据连接，同时刷新 Visio diagram 中所有可用的记录集。


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

