﻿---
title: Introduction
type: docs
weight: 10
url: /fr/net/introduction/
description: Introduction de la bibliothèque Aspose.Diagram.
---
## **Obtenez les informations sur le document Visio de la bibliothèque Aspose.Diagram for .NET**
Microsoft Visio enregistre des informations sur les actions entreprises sur un diagram dans le fichier. Par exemple, l'heure et la date de création du document, la dernière fois qu'il a été modifié, imprimé ou enregistré, sont enregistrées avec le fichier. Les informations sur la version de Microsoft Visio créée et la dernière modification du fichier sont également enregistrées.

Cet article explique comment récupérer ces informations.
### **Détermination de la version de Microsoft Visio qui a créé, modifié et enregistré un document**
 La propriété Version exposée par le[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/)et la propriété BuildNumberCreated exposée par la classe DocumentProperties est utilisée pour déterminer la version et le numéro de build complet de l'instance Microsoft Visio utilisée pour créer le document.

 La propriété BuildNumberEdited exposée par le[Propriétés du document](https://reference.aspose.com/diagram/net/aspose.diagram/documentproperties) La classe est utilisée pour déterminer le numéro de version complet de l'instance Microsoft Visio utilisée pour modifier le document.

Les propriétés TimeCreated, TimeEdited, TimePrinted et TimeSaved exposées par la classe DocumentProperties sont utilisées pour déterminer l'heure à laquelle le document Microsoft Visio a été créé, modifié pour la dernière fois, imprimé pour la dernière fois et enregistré pour la dernière fois.

Vous pouvez également définir ces propriétés pour modifier les informations du fichier. Les exemples de code ci-dessous montrent comment récupérer des informations sur la création du fichier ainsi que sur la date de création, de modification, d'impression et d'enregistrement.
#### **Exemple de programmation**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-GetLibraryVersion-GetLibraryVersion.cs" >}}
## **Rédaction d'informations sur le résumé du document Visio**
Microsoft Visio vous permet de définir un certain nombre de propriétés d'informations de résumé de document pour vous aider, vous et vos collègues, à identifier un diagram. Les propriétés de résumé, par exemple, le titre, le sujet, l'auteur et la description, rendent le fichier plus facile à trouver lors de la recherche et plus facile à reconnaître lorsque parcourir les fichiers.
### **Rédaction Microsoft Visio Résumé du document Info**
La classe DocumentProperties expose un certain nombre de propriétés pour définir ou obtenir les informations récapitulatives d'un Microsoft Visio diagram. Aspose.Diagram for .NET peut mettre à jour les informations récapitulatives du dessin, puis réécrire le fichier de dessin dans VDX.

{{% alert color="primary" %}} 

Veuillez noter que vous ne pouvez pas définir de valeurs par rapport au**Application**et**Producteur**champs, car Aspose Ltd. et Aspose.Diagram for .NET xxx seront affichés contre ces champs.

{{% /alert %}} 

Pour mettre à jour les informations récapitulatives du dessin d'un fichier VDX ou VSD existant :

1.  Créer une instance de[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/) classer.
1.  Définir les propriétés exposées par[Diagram.DocumentProps](https://reference.aspose.com/diagram/net/aspose.diagram/diagram/properties/documentprops) pour définir les informations récapitulatives du fichier de dessin Visio.
1. Appelez la méthode Save de la classe Diagram pour écrire le fichier de dessin Visio dans VDX.

Vérifiez les informations récapitulatives :

1. Ouvrez le fichier de sortie VDX dans Microsoft Visio.
1. Sélectionnez Info dans le menu Fichier.
#### **Rédaction Visio Exemple de programmation d'informations sur le résumé du document**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-SetVisioProperties-SetVisioProperties.cs" >}}
## **Détecter le format du fichier Visio**
En utilisant Aspose.Diagram for .NET API, les développeurs peuvent détecter le format du fichier Visio avant de l'ouvrir car l'extension de fichier ne garantit pas que le contenu du fichier est approprié.
### **Détecter l'échantillon de programmation de format**
L'exemple de code suivant montre comment détecter un format de fichier (à l'aide du chemin d'accès au fichier ou du flux) et vérifier son extension.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Introduction-DetectVisioFileFormat-DetectVisioFileFormat.cs" >}}
