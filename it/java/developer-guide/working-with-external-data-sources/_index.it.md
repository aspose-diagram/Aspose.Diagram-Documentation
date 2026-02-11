---
title: Utilizzo di origini dati esterne
type: docs
weight: 190
url: /it/java/working-with-external-data-sources/
---
## **Aggiornamento Connessione Dati del Disegno Visio**
Aspose.Diagram API consente agli utenti di modificare la connessione dati di SQL Server del disegno Visio collegato. Per inserire i dati nel disegno Visio, è necessario accedere ai dati di SQL Server. Assicurarsi che il database non sia aperto in modalità esclusiva.

 Ora è un fenomeno comune collegare i dati dei diagrammi Microsoft Visio dalle fonti di dati esterne. Il[DataConnectionCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/dataconnectioncollection) class contiene tutte le connessioni dati.
### **Esempio di programmazione**
La parte di codice seguente modifica una particolare connessione dati e aggiorna anche tutti i set di record disponibili in Visio diagram.

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
