---
title: Définir Visio les données XForm, Line et Fill de la forme
type: docs
weight: 70
url: /fr/java/set-visio-shape-s-xform-line-and-fill-data/
---
## **Définition des données XForm**
 L'élément XForm fait partie du schéma XML Microsoft Visio. XForm spécifie une position de formes, par exemple la largeur, la hauteur, la rotation et si la forme a été retournée. La[XForm](https://reference.aspose.com/diagram/java/com.aspose.diagram/xform) propriété, exposée par la[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) classe, prend en charge l'objet Aspose.Diagram.XForm. La propriété XForm peut être utilisée pour récupérer ou mettre à jour les données XForm d'une forme. Les exemples de code de cet article modifient les valeurs XForm PinX (coordonnée X) et PinY (coordonnée Y) pour déplacer les formes sur la page.

**Entrée diagram** 

![tâche : image_autre_texte](set-visio-shape-s-xform-line-and-fill-data_1.png)

**Le diagram après le** **PinX** **et** **PinY** **les valeurs ont été modifiées** 

![tâche : image_autre_texte](set-visio-shape-s-xform-line-and-fill-data_2.png)

Le processus de mise à jour des données XForm est :

1. Charger un diagram.# Trouver une forme particulière.# Mettre à jour les données XForm de la forme.
1. Enregistrez le diagram.
### **Exemple de programmation**
L'extrait de code ci-dessous montre comment mettre à jour les données XForm d'une forme. Le code recherche un processus de noms de forme, avec l'ID de forme 1, et définit ses coordonnées X et Y sur 5.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SetXFormdata-SetXFormdata.java" >}}
## **Définir les données de ligne de la forme Visio**
Les formes peuvent être formatées de plusieurs manières. Cet article explique comment spécifier les attributs d'une ligne.

Microsoft Visio permet aux utilisateurs de formater les lignes de différentes manières. Aspose.Diagram for Java prend en charge :

- Poids : l'épaisseur d'une ligne.
- Couleur : définissez la couleur de la ligne de la forme.
- Transparence de la couleur de la ligne : définissez la transparence de la couleur de la ligne de la forme en pourcentage.
- Motif : définit si la ligne est pleine, en pointillés ou a un autre motif.
- Arrondi : le rayon des coins.
- Flèches de début et de fin : indiquez si la ligne comporte des flèches.
- Tailles des flèches de début et de fin : définissez les tailles des flèches.
- Cap : l'arrondi de la ligne se termine.
### **Modifier la couleur de la ligne, l'épaisseur, le type de tiret, la transparence, l'arrondi, le type de flèche et la taille de la flèche de la bordure d'une forme**
 La[Ligne](https://reference.aspose.com/diagram/java/com.aspose.diagram/line) propriété, exposée par la[Forme](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)classe, prend en charge l'objet Aspose.Diagram.Line. Cette propriété peut être utilisée pour récupérer ou mettre à jour les données de ligne d'une forme.
#### **Exemple de programmation de données de ligne**
Le morceau de code suivant met à jour les données de ligne de shape.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SetLineData-SetLineData.java" >}}
## **Définir les données de remplissage de la forme Visio**
Les formes peuvent être formatées de plusieurs manières. Cette rubrique décrit comment spécifier le remplissage d'une forme.

 Microsoft Office Visio permet aux utilisateurs de formater les remplissages de différentes manières. La[Remplir](https://reference.aspose.com/diagram/java/com.aspose.diagram/fill) classe du Aspose.Diagram for Java API prend en charge le réglage :

- Couleurs de fond et de premier plan.
- Transparence.
- Motifs de remplissage.
- Ombres.
### **Définition des valeurs de remplissage**
La propriété Fill, exposée par la classe Shape, prend en charge l'objet Aspose.Diagram.Fill. La propriété Fill peut être utilisée pour récupérer ou mettre à jour les données de remplissage d'une forme.

|<p>**L'entrée diagram** </p><p>![tâche : image_autre_texte](http://i.imgur.com/OrhEecb.png)</p>|<p>**Le diagram après avoir changé la couleur de remplissage** </p><p>![tâche : image_autre_texte](http://i.imgur.com/HO0wmZ8.png)</p>|
|:- |:- |
#### **Exemple de programmation de données de remplissage**
L'extrait de code suivant met à jour les données de remplissage d'une forme. Le code recherche une forme nommée rectangle, avec l'ID de forme 1, et définit les couleurs de remplissage d'arrière-plan et de premier plan.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SetFillData-SetFillData.java" >}}
### **Récupérer les données de remplissage héritées d'une forme Visio**
Les formes Visio peuvent hériter du style parent et de la forme principale. Les développeurs peuvent obtenir ou définir les données de remplissage héritées d'une forme Visio. La propriété InheritFill, exposée par la classe Shape, contient les valeurs de formatage de remplissage pour la forme héritée par le style parent et la forme principale.
#### **Récupérer un exemple de programmation de données de remplissage héritées**
L'extrait de code suivant récupère les données de remplissage héritées de la forme. Veuillez vérifier cet exemple de code :

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveInheritedFillData-RetrieveInheritedFillData.java" >}}
