---
title: Travailler avec des sources de données externes
type: docs
weight: 200
url: /fr/net/working-with-external-data-sources/
description: Cette section explique comment travailler avec des sources de données externes avec Aspose.Diagram.
---
## **Modifier la connexion de données SQL Server et actualiser les jeux d'enregistrements**
Aspose.Diagram API permet aux utilisateurs de modifier la connexion de données SQL Server et d'actualiser tous les jeux d'enregistrements. Pour importer des données dans le dessin Visio, nous avons besoin d'accéder aux données SQL Server. Assurez-vous que la base de données n'est pas ouverte en mode exclusif.
### **Mettre à jour la connexion de données et les ensembles d'enregistrements**
 C'est maintenant un phénomène courant de lier les données des diagrammes Microsoft Visio à partir des sources de données externes. La[DataConnectionCollectionDataConnectionCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/dataconnectioncollection) classe contient toutes les connexions de données.
#### **Exemple de programmation**
Le morceau de code suivant modifie une connexion de données particulière et actualise également tous les jeux d'enregistrements disponibles dans le Visio diagram.

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
