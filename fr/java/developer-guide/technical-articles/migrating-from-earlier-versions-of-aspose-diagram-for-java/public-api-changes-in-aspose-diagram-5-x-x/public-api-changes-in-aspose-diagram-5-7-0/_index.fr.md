---
title: Public API Changements dans Aspose.Diagram 5.7.0
type: docs
weight: 30
url: /fr/java/public-api-changes-in-aspose-diagram-5-7-0/
---
{{% alert color="primary" %}} 

Ce document décrit les modifications apportées au Aspose.Diagram API de la version 5.6.0 à 5.7.0, qui peuvent intéresser les développeurs de modules/applications. Il comprend non seulement des méthodes publiques nouvelles et mises à jour, mais également une description de tout changement de comportement dans les coulisses de Aspose.Diagram.

{{% /alert %}} 
### **Définir les chaînes de modèle de date sur la chronologie**
Les nouvelles méthodes setDateFormatStringForBE et setDateFormatStringForIntm ont été ajoutées dans la classe TimelineHelper. Exemples de codes :

**Java**

{{< highlight "java" >}}

 // set DateFormat String for start and finish of timeline shape

timelineHelper.setDateFormatStringForBE("yyyy-MM-dd");

// set DateFormat String for intm of timeline shape

timelineHelper.setDateFormatStringForIntm("yyyy-MM-dd");

{{< /highlight >}}
