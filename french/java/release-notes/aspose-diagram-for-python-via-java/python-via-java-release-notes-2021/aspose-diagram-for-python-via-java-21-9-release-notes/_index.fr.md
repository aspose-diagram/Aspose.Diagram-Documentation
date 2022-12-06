---
title: Aspose.Diagram pour Python via Java 21.9 Notes de mise à jour
type: docs
weight: 6
url: /fr/java/aspose-diagram-for-python-via-java-21-9-release-notes/
---
{{% alert color="primary" %}}

Cette page contient des informations sur les notes de version pour Aspose.Diagram pour Python via Java 21.9.

{{% /alert %}}
## **Améliorations et changements**  ##

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMJAVA-50753|wk : Vérifiez si TextAnnotation est connecté à la forme|Renforcement|
|DIAGRAMJAVA-50382|L'ombrage des formes est manquant lors de la conversion d'un VSDX en PDF|Punaise|
|DIAGRAMJAVA-50754|wk - LineColor de InheritLine n'est pas correct|Punaise|
|DIAGRAMJAVA-50756|wk : PinPos nul vs centre-centre|Punaise|
|DIAGRAMJAVA-50757|WK : valeur getBegin/End Arrow incorrecte.|Punaise|
|DIAGRAMJAVA-50771|WK : impossible d'obtenir LineColor et le nom de la forme de la feuille|Punaise|
## `?`**Public API et modifications incompatibles avec les versions antérieures**
Vous trouverez ci-dessous une liste de toutes les modifications apportées au public API, telles que les membres ajoutés, renommés, supprimés ou obsolètes, ainsi que toute modification non rétrocompatible apportée à Aspose.Diagram for Java. Si vous avez des inquiétudes concernant l'un des changements répertoriés, veuillez le signaler sur le forum d'assistance Aspose.Diagram.

### **Ajoute dependOnShapes dans Shape**
- Renvoie un tableau qui contient les identifiants des formes qui dépendent d'une forme.



{{< highlight "java" >}}

long[]shapeids = shape.dependsOnShapes();

{{< /highlight >}}