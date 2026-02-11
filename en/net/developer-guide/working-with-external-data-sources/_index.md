---
title: Working with External Data Sources
type: docs
weight: 200
url: /net/working-with-external-data-sources/
description: This section explains how to working with external data sources with Aspose.Diagram.
---

## **Edit SQL Server Data Connection and Refresh Record Sets**
Aspose.Diagram API allows users to edit SQL Server data connection and refresh all the record sets. To bring data into the Visio drawing, we need access to the SQL Server data. Make sure that the database is not opened in exclusive mode.
### **Update Data Connection and Record Sets**
It's now a common phenomena to link the data of Microsoft Visio diagrams from the external data sources. The [DataConnectionCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/dataconnectioncollection) class contains all the data connections.
#### **Programming Sample**
The following piece of code edits a particular data connection and also refresh all the available record sets in the Visio diagram.


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

