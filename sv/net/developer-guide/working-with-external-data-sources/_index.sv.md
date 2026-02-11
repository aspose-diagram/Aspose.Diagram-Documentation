---
title: Arbeta med externa datakällor
type: docs
weight: 200
url: /sv/net/working-with-external-data-sources/
description: Det här avsnittet förklarar hur du arbetar med externa datakällor med Aspose.Diagram.
---
## **Redigera SQL Server Data Connection och Refresh Record Sets**
Aspose.Diagram API tillåter användare att redigera SQL Server-dataanslutning och uppdatera alla postuppsättningar. För att få in data i Visio-ritningen behöver vi tillgång till SQL Server-data. Se till att databasen inte öppnas i exklusivt läge.
### **Uppdatera dataanslutning och postuppsättningar**
 Det är nu ett vanligt fenomen att länka data från Microsoft Visio diagram från externa datakällor. De[DataConnectionCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/dataconnectioncollection) klass innehåller alla dataanslutningar.
#### **Programmeringsexempel**
Följande kod redigerar en viss dataanslutning och uppdaterar även alla tillgängliga postuppsättningar i Visio diagram.


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

