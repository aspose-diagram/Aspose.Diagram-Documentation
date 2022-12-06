---
title: Aspose.Diagram for Java 20.1 Notes de mise à jour
type: docs
weight: 70
url: /fr/java/aspose-diagram-for-java-20-1-release-notes/
---
{{% alert color="primary" %}} 

Cette page contient des informations sur les notes de version pour Aspose.Diagram for Java 20.1.

{{% /alert %}} 
## **Améliorations et changements**

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMJAVA-50664|Remplissage dégradé non pris en charge lors de l'exportation vers SVG|Renforcement|
|DIAGRAMJAVA-50670|Autoriser le chargement des polices depuis la mémoire|Renforcement|
|DIAGRAMJAVA-50681|API prend beaucoup de temps pour charger le fichier diagram de grande taille|Renforcement|
|DIAGRAMJAVA-50381|Les formes de réseau ne sont pas conservées lors de la conversion d'un VSDX en PDF|Punaise|
|DIAGRAMJAVA-50386|Les images sont inversées avec une différence de couleur lors de la conversion d'un VSD en SVG|Punaise|
|DIAGRAMJAVA-50679|VSDX au format PDF - Les connecteurs manquent dans la sortie|Punaise|
|DIAGRAMJAVA-50680|Visio en PNG - Les images de sortie ont été rognées|Punaise|
## **Public API et modifications incompatibles avec les versions antérieures**
Voici une liste de toutes les modifications apportées au API public, telles que les membres ajoutés, renommés, supprimés ou obsolètes, ainsi que toute modification non rétrocompatible apportée au Aspose.Diagram pour JAVA. Si vous avez des inquiétudes concernant un changement répertorié, veuillez le signaler sur le forum d'assistance Aspose.Diagram.

- GetPages et setPages ajoutés dans la page - Spécifie l'index des pages à charger.

{{< highlight "java" >}}

 LoadOptions options = new LoadOptions(LoadFileFormat.VSDX);

options.setPages(new ArrayList());

options.getPages().add(0);

{{< /highlight >}}

- Ajoute setFontSources dans FontConfigs - Définit les sources des polices.

{{< highlight "java" >}}

 byte[]b = new byte[]{ 0 };

com.aspose.diagram.MemoryFontSource sc1 = new com.aspose.diagram.MemoryFontSource(b);

com.aspose.diagram.MemoryFontSource sc2 = new com.aspose.diagram.MemoryFontSource(b);

com.aspose.diagram.MemoryFontSource[]sc = new com.aspose.diagram.MemoryFontSource[]{ sc1, sc2 };

com.aspose.diagram.FontConfigs.setFontSources(sc); 

{{< /highlight >}}


