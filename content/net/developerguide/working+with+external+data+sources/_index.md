---
title : "Working with External Data Sources" 
description : "" 
weight : 8052 
toc : false
type: docs
url: /net/developerguide/working+with+external+data+sources/
---

# Aspose.Diagram for .NET : Working with External Data Sources


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Edit SQL Server Data Connection and Refresh Record Sets](#edit-sql-server-data-connection-and-refresh-record-sets)
    *   1.1 [Update Data Connection and Record Sets](#update-data-connection-and-record-sets)
        *   1.1.1 [Programming Sample](#programming-sample)
{{< /panel >}}
 

 

## Edit SQL Server Data Connection and Refresh Record Sets

Aspose.Diagram API allows users to edit SQL Server data connection and refresh all the record sets. To bring data into the Visio drawing, we need access to the SQL Server data. Make sure that the database is not opened in exclusive mode.

### Update Data Connection and Record Sets

It's now a common phenomena to link the data of Microsoft Visio diagrams from the external data sources. The [DataConnectionCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/dataconnectioncollection) class contains all the data connections.

#### Programming Sample

The following piece of code edits a particular data connection and also refresh all the available record sets in the Visio diagram.

