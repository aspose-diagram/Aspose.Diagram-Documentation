---
title: Working with External Data Sources
type: docs
weight: 190
url: /java/working-with-external-data-sources/
---

## **Update Data Connection of the Visio Drawing**
Aspose.Diagram API allows users to edit SQL Server data connection of the linked Visio drawing. To bring data into the Visio drawing, we need access to the SQL Server data. Make sure that the database is not opened in exclusive mode.

It's now a common phenomena to link the data of Microsoft Visio diagrams from the external data sources. The [DataConnectionCollection](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/DataConnectionCollection) class contains all the data connections.
### **Programming Sample**
The following piece of code edits a particular data connection and also refresh all the available record sets in the Visio diagram.

{{< gist "aspose-diagram" "92a05cb833bad6d60de2968c96b40ee4" "Examples-src-main-java-com-aspose-diagram-examples-ExternalDataSources-EditDataConAndRefreshRecords-EditDataConAndRefreshRecords.java" >}}
