---
title: Working with External Data Sources
type: docs
weight: 190
url: /java/working-with-external-data-sources/
---

## **Update Data Connection of the Visio Drawing**
Aspose.Diagram API allows users to edit SQL Server data connection of the linked Visio drawing. To bring data into the Visio drawing, we need access to the SQL Server data. Make sure that the database is not opened in exclusive mode.

It's now a common phenomena to link the data of Microsoft Visio diagrams from the external data sources. The [DataConnectionCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/dataconnectioncollection) class contains all the data connections.
### **Programming Sample**
The following piece of code edits a particular data connection and also refresh all the available record sets in the Visio diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-ExternalDataSources-EditDataConAndRefreshRecords-EditDataConAndRefreshRecords.java" >}}
