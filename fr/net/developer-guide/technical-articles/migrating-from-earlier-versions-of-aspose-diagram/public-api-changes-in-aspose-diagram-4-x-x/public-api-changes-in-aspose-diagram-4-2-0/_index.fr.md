---
title: Public API Changements dans Aspose.Diagram 4.2.0
type: docs
weight: 30
url: /fr/net/public-api-changes-in-aspose-diagram-4-2-0/
---
{{% alert color="primary" %}} 

Ce document décrit les modifications apportées au Aspose.Diagram API de la version 4.1.0 à 4.2.0, qui peuvent intéresser les développeurs de modules/applications. Il comprend non seulement des méthodes publiques nouvelles et mises à jour, mais également une description de tout changement de comportement dans les coulisses de Aspose.Diagram.

{{% /alert %}} 
## **Ajoute deux méthodes GetMasterByName et IsExist à MasterCollection**
Les développeurs peuvent désormais coller des formes de groupe à l'intérieur du conteneur. De plus, cette version permet d'obtenir le Master par son nom et de vérifier la présence du Master par son nom. Vous pouvez voir des exemples de rubriques sur ces fonctionnalités : [Get Master Object from the Visio], [Check Presence of a Master in the Visio Drawing]## **Ajoute une méthode GlueShapesInContainer à Page**
Auparavant, cela fonctionnait parfaitement avec les formes dissociées. Cependant, il y a beaucoup de points dans les formes de groupe, ce n'était pas si bien supporté. Nous avons maintenant ajouté la prise en charge des formes de groupe. Veuillez consulter un exemple de sujet sur cette fonctionnalité : [Coller la forme du groupe à l'intérieur du conteneur]