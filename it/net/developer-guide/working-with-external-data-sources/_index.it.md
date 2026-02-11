---
title: Utilizzo di origini dati esterne
type: docs
weight: 200
url: /it/net/working-with-external-data-sources/
description: Questa sezione spiega come lavorare con origini dati esterne con Aspose.Diagram.
---
## **Modifica la connessione dati di SQL Server e aggiorna i set di record**
Aspose.Diagram API consente agli utenti di modificare la connessione dati di SQL Server e aggiornare tutti i set di record. Per portare i dati nel disegno Visio, è necessario accedere ai dati di SQL Server. Assicurarsi che il database non sia aperto in modalità esclusiva.
### **Aggiorna connessione dati e set di record**
 Ora è un fenomeno comune collegare i dati dei diagrammi Microsoft Visio dalle fonti di dati esterne. Il[DataConnectionCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/dataconnectioncollection) class contiene tutte le connessioni dati.
#### **Esempio di programmazione**
La parte di codice seguente modifica una particolare connessione dati e aggiorna anche tutti i set di record disponibili in Visio diagram.

```
{{< highlight "csharp" >}}
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
```
