---
title: Arbeiten mit externen Datenquellen
type: docs
weight: 190
url: /de/java/working-with-external-data-sources/
---
## **Aktualisieren Sie die Datenverbindung der Zeichnung Visio**
Aspose.Diagram API ermöglicht Benutzern, die SQL Server-Datenverbindung der verknüpften Visio-Zeichnung zu bearbeiten. Um Daten in die Zeichnung Visio zu bringen, benötigen wir Zugriff auf die SQL Server-Daten. Stellen Sie sicher, dass die Datenbank nicht im exklusiven Modus geöffnet ist.

 Es ist mittlerweile ein weit verbreitetes Phänomen, die Daten von Microsoft Visio Diagrammen aus externen Datenquellen zu verknüpfen. Das[DataConnectionCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/dataconnectioncollection) Klasse enthält alle Datenverbindungen.
### **Programmierbeispiel**
Der folgende Codeabschnitt bearbeitet eine bestimmte Datenverbindung und aktualisiert auch alle verfügbaren Datensätze in Visio diagram.

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
