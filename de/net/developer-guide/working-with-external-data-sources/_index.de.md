---
title: Arbeiten mit externen Datenquellen
type: docs
weight: 200
url: /de/net/working-with-external-data-sources/
description: In diesem Abschnitt wird erläutert, wie Sie mit Aspose.Diagram mit externen Datenquellen arbeiten.
---
## **Bearbeiten Sie die SQL Server-Datenverbindung und aktualisieren Sie Datensätze**
Aspose.Diagram API ermöglicht Benutzern, die SQL Server-Datenverbindung zu bearbeiten und alle Datensätze zu aktualisieren. Um Daten in die Zeichnung Visio zu bringen, benötigen wir Zugriff auf die SQL Server-Daten. Stellen Sie sicher, dass die Datenbank nicht im exklusiven Modus geöffnet ist.
### **Datenverbindung und Datensätze aktualisieren**
 Es ist mittlerweile ein weit verbreitetes Phänomen, die Daten von Microsoft Visio Diagrammen aus externen Datenquellen zu verknüpfen. Das[DataConnectionCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/dataconnectioncollection) Klasse enthält alle Datenverbindungen.
#### **Programmierbeispiel**
Der folgende Codeabschnitt bearbeitet eine bestimmte Datenverbindung und aktualisiert auch alle verfügbaren Datensätze in Visio diagram.

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
