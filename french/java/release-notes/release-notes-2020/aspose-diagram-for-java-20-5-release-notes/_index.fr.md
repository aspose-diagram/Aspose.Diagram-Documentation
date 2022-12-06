---
title: Aspose.Diagram for Java 20.5 Notes de mise à jour
type: docs
weight: 30
url: /fr/java/aspose-diagram-for-java-20-5-release-notes/
---
{{% alert color="primary" %}} 

Cette page contient des informations sur les notes de version pour Aspose.Diagram for Java 20.5.

{{% /alert %}} 
## **Améliorations et changements**

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMJAVA-50487|Éléments de texte déplacés lors de la conversion d'un VSD en SVG|Renforcement|
|DIAGRAMJAVA-50692|Texte en gras mal positionné lors de l'enregistrement de VSDX au format SVG|Renforcement|
|DIAGRAMJAVA-50693|Les images ne sont pas présentes dans la sortie SVG|Punaise|
|DIAGRAMJAVA-50695|Impossible d'enregistrer le fichier VSDX en tant qu'image - il lève NullPointerException|Punaise|
## **Public API et modifications incompatibles avec les versions antérieures**
Voici une liste de toutes les modifications apportées au API public, telles que les membres ajoutés, renommés, supprimés ou obsolètes, ainsi que toute modification non rétrocompatible apportée au Aspose.Diagram pour JAVA. Si vous avez des inquiétudes concernant un changement répertorié, veuillez le signaler sur le forum d'assistance Aspose.Diagram.
### **Ajoute isIntersect dans Shape**
Indique si cette forme croise une autre forme.

{{< highlight "java" >}}

 boolean isIntersect = s1.isIntersect(s2);

{{< /highlight >}}
