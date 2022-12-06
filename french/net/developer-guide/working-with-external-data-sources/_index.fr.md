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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-External-Data-Sources-EditDataConAndRefreshRecords-EditDataConAndRefreshRecords.cs" >}}
