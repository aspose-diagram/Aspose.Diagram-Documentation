---
title: Aspose.Diagram for Java 18.2 Notes de mise à jour
type: docs
weight: 110
url: /fr/java/aspose-diagram-for-java-18-2-release-notes/
---
{{% alert color="primary" %}} 

 Cette page contient des notes de version pour[Aspose.Diagram for Java 18.2](https://docs.aspose.com/diagram/java/aspose-diagram-for-java-18-2-release-notes/).

{{% /alert %}} 
## **Améliorations et changements**

|**Clé**|**Sommaire**|**Catégorie**|
|:- |:- |:- |
|DIAGRAMJAVA-50587|Ajout de la prise en charge de la récupération de l'élément Char relatif de la partie texte|Renforcement|
|DIAGRAMJAVA-50478|Les lignes de connexion passent par les autres formes lors de la conversion d'un VDX en VSDM|Punaise|
|DIAGRAMJAVA-50581|VSDX au format PDF - rendu incorrect des formes|Punaise|
|DIAGRAMJAVA-50582|Sortie VSDX - les lignes de connexion ne sont pas droites|Punaise|
|DIAGRAMJAVA-50583|VSD import - une erreur s'est produite dans l'élément VisioDocument|Punaise|
|DIAGRAMJAVA-50584|VDX import - une erreur s'est produite dans l'élément VisioDocument|Punaise|
|DIAGRAMJAVA-50585|VSD import - une erreur s'est produite dans l'élément VisioDocument|Punaise|
|DIAGRAMJAVA-50586|VSDX vers SVG - couleur de bordure incorrecte de la forme|Punaise|
### **Ajoute la méthode getInheritChars dans la classe Shape**
Il contient les valeurs char pour la forme héritée par la forme principale.

{{< highlight "java" >}}

 CharCollection charCollection = shape.getInheritChars();

{{< /highlight >}}
