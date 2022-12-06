---
title: Définir Visio les données XForm, Line et Fill de la forme
type: docs
weight: 20
url: /fr/net/set-visio-shape-s-xform-line-and-fill-data/
description: Cette section explique comment définir le style de la forme, y compris ses données de ligne et remplir les données avec Aspose.Diagram.
---
## **Définition des données XForm**
 L'élément XForm fait partie du schéma XML Microsoft Visio. XForm spécifie une position de formes, par exemple la largeur, la hauteur, la rotation et si la forme a été retournée. La[XForm](http://www.aspose.com/api/net/diagram/aspose.diagram/xform) propriété, exposée par la[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) classe, prend en charge l'objet Aspose.Diagram.XForm. La propriété XForm peut être utilisée pour récupérer ou mettre à jour les données XForm d'une forme. Les exemples de code de cet article modifient les valeurs XForm PinX (coordonnée X) et PinY (coordonnée Y) pour déplacer les formes sur la page.

Le processus de mise à jour des données XForm est :

1. Charger un diagram.# Trouver une forme particulière.# Mettre à jour les données XForm de la forme.
1. Enregistrez le diagram.
### **Exemple de programmation**
L'extrait de code ci-dessous montre comment mettre à jour les données XForm d'une forme. Le code recherche un processus de noms de forme, avec l'ID de forme 1, et définit ses coordonnées X et Y sur 5.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetXFormdata-SetXFormdata.cs" >}}
## **Définir les données de ligne de la forme Visio**
Les formes peuvent être formatées de plusieurs manières. Cet article explique comment spécifier les attributs d'une ligne.

Microsoft Visio permet aux utilisateurs de formater les lignes de différentes manières. Aspose.Diagram for .NET prend en charge :

- Poids : l'épaisseur d'une ligne.
- Couleur : définissez la couleur de la ligne de la forme.
- Transparence de la couleur de la ligne : définissez la transparence de la couleur de la ligne de la forme en pourcentage.
- Motif : définit si la ligne est pleine, en pointillés ou a un autre motif.
- Arrondi : le rayon des coins.
- Flèches de début et de fin : indiquez si la ligne comporte des flèches.
- Tailles des flèches de début et de fin : définissez les tailles des flèches.
- Cap : l'arrondi de la ligne se termine.
### **Modifier la couleur de la ligne, l'épaisseur, le type de tiret, la transparence, l'arrondi, le type de flèche et la taille de la flèche de la bordure d'une forme**
 La[Ligne](http://www.aspose.com/api/net/diagram/aspose.diagram/line) propriété, exposée par la[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)classe, prend en charge l'objet Aspose.Diagram.Line. Cette propriété peut être utilisée pour récupérer ou mettre à jour les données de ligne d'une forme.
#### **Exemple de programmation de données de ligne**
Le morceau de code suivant met à jour les données de ligne de shape.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetLineData-SetLineData.cs" >}}
## **Définir les données de remplissage de la forme Visio**
 Les formes peuvent être formatées de plusieurs manières. Cette rubrique décrit comment spécifier le remplissage d'une forme. Microsoft Office Visio permet aux utilisateurs de formater les remplissages de différentes manières. La[Remplir](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) classe du Aspose.Diagram for .NET API prend en charge le réglage :

- Couleurs de fond et de premier plan.
- Transparence.
- Motifs de remplissage.
- Ombres.
### **Définition des valeurs de remplissage**
 La propriété Fill, exposée par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) classe, prend en charge la[Aspose.Diagram.Fill](http://www.aspose.com/api/net/diagram/aspose.diagram/fill) objet. La propriété Fill peut être utilisée pour récupérer ou mettre à jour les données de remplissage d'une forme.
#### **Exemple de programmation de données de remplissage**
L'extrait de code suivant met à jour les données de remplissage d'une forme. Le code recherche une forme nommée rectangle, avec l'ID de forme 1, et définit les couleurs de remplissage d'arrière-plan et de premier plan.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-SetFillData-SetFillData.cs" >}}
### **Récupérer les données de remplissage héritées d'une forme Visio**
 Les formes Visio peuvent hériter du style parent et de la forme principale. Les développeurs peuvent obtenir ou définir les données de remplissage héritées d'une forme Visio. La propriété InheritFill, exposée par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) classe, contient les valeurs de formatage de remplissage pour la forme héritée par le style parent et la forme principale.
#### **Récupérer un exemple de programmation de données de remplissage héritées**
L'extrait de code suivant récupère les données de remplissage héritées de la forme. Veuillez vérifier cet exemple de code :

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RetrieveInheritedFillData-RetrieveInheritedFillData.cs" >}}
