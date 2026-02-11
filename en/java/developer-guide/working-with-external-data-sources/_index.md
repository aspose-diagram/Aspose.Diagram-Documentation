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

```
{{< highlight "java" >}}
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
```
