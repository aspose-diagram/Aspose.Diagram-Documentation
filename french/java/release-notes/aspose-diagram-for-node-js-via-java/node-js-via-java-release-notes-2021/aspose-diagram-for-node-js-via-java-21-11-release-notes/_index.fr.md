---
title: Aspose.Diagram pour Node.js via Java 21.11 Notes de version
type: docs
weight: 4
url: /fr/java/aspose-diagram-for-node-js-via-java-21-11-release-notes/
---
{{% alert color="primary" %}}

Cette page contient des informations sur les notes de publication pour Aspose.Diagram pour Node.js via Java 21.11.

{{% /alert %}}
## **Améliorations et changements**  ##

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMJAVA-50806|wk : InheridetChar Color|Renforcement|
|DIAGRAMJAVA-50385|La couleur de la bordure et des titres est modifiée lors de la conversion d'un VSDX en PDF|Punaise|
|DIAGRAMJAVA-50501|VSDX vers PNG - Mauvaise couleur des formes|Punaise|
|DIAGRAMJAVA-50631|Les formes sont incohérentes après l'exportation de VSDX au format PDF|Punaise|
|DIAGRAMJAVA-50804|Le texte du connecteur est renvoyé à la ligne lors du dessin du connecteur|Punaise|
## `?`**Public API et modifications incompatibles avec les versions antérieures**
Vous trouverez ci-dessous une liste de toutes les modifications apportées au public API, telles que les membres ajoutés, renommés, supprimés ou obsolètes, ainsi que toute modification non rétrocompatible apportée à Aspose.Diagram for Java. Si vous avez des inquiétudes concernant l'un des changements répertoriés, veuillez le signaler sur le forum d'assistance Aspose.Diagram.

### **Ajoute PresetTheme dans Shape**
- Appliquez un thème prédéfini à cette forme.

{{< highlight "java" >}}
 
 shape.setPresetTheme( PresetThemeValue.BUBBLE);

{{< /highlight >}}


### **Ajoute PresetThemeVariant dans Shape**
- Appliquer une variante de thème prédéfinie à cette forme

{{< highlight "java" >}}

shape.setPresetThemeVariant( PresetThemeVariantValue.VARIANT_1);

{{< /highlight >}}

### **Ajoute PresetThemeQuickStyle dans Shape**
- Appliquer un style rapide de variante de thème prédéfini à cette forme

{{< highlight "java" >}}

shape.setPresetThemeQuickStyle(PresetQuickStyleValue.VARIANT_STYLE_1);

{{< /highlight >}}
