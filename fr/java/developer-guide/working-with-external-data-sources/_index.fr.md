---
title: Travailler avec des sources de données externes
type: docs
weight: 190
url: /fr/java/working-with-external-data-sources/
---
## **Mettre à jour la connexion de données du dessin Visio**
Aspose.Diagram API permet aux utilisateurs de modifier la connexion de données SQL Server du dessin Visio lié. Pour importer des données dans le dessin Visio, nous avons besoin d'accéder aux données SQL Server. Assurez-vous que la base de données n'est pas ouverte en mode exclusif.

 C'est maintenant un phénomène courant de lier les données des diagrammes Microsoft Visio à partir des sources de données externes. La[DataConnectionCollectionDataConnectionCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/dataconnectioncollection) classe contient toutes les connexions de données.
### **Exemple de programmation**
Le morceau de code suivant modifie une connexion de données particulière et actualise également tous les jeux d'enregistrements disponibles dans le Visio diagram.

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
