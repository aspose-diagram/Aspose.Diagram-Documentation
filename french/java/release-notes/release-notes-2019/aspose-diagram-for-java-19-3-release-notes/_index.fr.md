---
title: Aspose.Diagram for Java 19.3 Notes de mise à jour
type: docs
weight: 100
url: /fr/java/aspose-diagram-for-java-19-3-release-notes/
---
{{% alert color="primary" %}} 

Cette page contient les notes de version pour Aspose.Diagram for Java 19.3

{{% /alert %}} 
## **Améliorations et changements**

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMJAVA-50339|Ajout de la prise en charge de la récupération des répertoires de polices communs sur les systèmes d'exploitation|Renforcement|
|DIAGRAMJAVA-50097|Conversion VSD en PDF - Les lignes courbes deviennent une ligne droite|Punaise|
|DIAGRAMJAVA-50161|Conversion VTX en HTML - L'image d'arrière-plan de l'ensemble diagram est manquante|Punaise|
|DIAGRAMJAVA-50301|VSD vers exportation PDF - Les formes de type méta se transforment en symboles désordonnés|Punaise|
|DIAGRAMJAVA-50464|La forme s'est mal rendue lors de la conversion de VSDX en PNG|Punaise|
|DIAGRAMJAVA-50652|VISIO en PDF - Le PDF de sortie affiche une erreur dans Adobe Reader|Punaise|
## **Public API et modifications incompatibles avec les versions antérieures**
Voici une liste de toutes les modifications apportées au public API, telles que les membres ajoutés, renommés, supprimés ou obsolètes, ainsi que toute modification non rétrocompatible apportée à Aspose.Diagram for Java. Si vous avez des préoccupations concernant l'un des changements répertoriés, veuillez les signaler dans la[Aspose.Diagram forum d'assistance](https://forum.aspose.com/c/diagram/17).
### **Ajoute GetDefaultFontDir dans Diagram**
Obtenir le chemin du dossier des polices par défaut

{{< highlight "java" >}}

  string str =  diagram.getDefaultFontDir();

{{< /highlight >}}
