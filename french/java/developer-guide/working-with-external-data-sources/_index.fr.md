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

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-ExternalDataSources-EditDataConAndRefreshRecords-EditDataConAndRefreshRecords.java" >}}
