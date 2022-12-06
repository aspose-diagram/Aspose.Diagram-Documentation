---
title: 使用外部数据源
type: docs
weight: 200
url: /zh/net/working-with-external-data-sources/
description: 本节介绍如何使用 Aspose.Diagram 使用外部数据源。
---
## **编辑 SQL Server 数据连接和刷新记录集**
Aspose.Diagram API 允许用户编辑 SQL Server 数据连接并刷新所有记录集。要将数据引入 Visio 绘图，我们需要访问 SQL Server 数据。确保数据库未以独占模式打开。
### **更新数据连接和记录集**
从外部数据源链接Microsoft Visio图表的数据现在是一种普遍现象。这[数据连接集合](http://www.aspose.com/api/net/diagram/aspose.diagram/dataconnectioncollection)类包含所有数据连接。
#### **编程范例**
下面的一段代码编辑一个特定的数据连接，同时刷新 Visio diagram 中所有可用的记录集。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-External-Data-Sources-EditDataConAndRefreshRecords-EditDataConAndRefreshRecords.cs" >}}
