---
title: Aspose.Diagram Modèle d'objet
linktitle: Aspose.Diagram Modèle d'objet
type: docs
description: Le modèle d'objet Aspose.Diagram fournit des informations sur les relations structurelles entre les objets de la bibliothèque de classes Aspose.Diagram.
weight: 20
url: /fr/net/object_model
---
{{% alert color="primary" %}} 

**Aspose.Diagram Modèle d'objet**

Le modèle d'objet Aspose.Diagram fournit des informations sur les relations structurelles entre les objets de la bibliothèque de classes Aspose.Diagram.

{{% /alert %}} 

### La structure de niveau supérieur du modèle d'objet Aspose.Diagram est présentée ci-dessous de manière hiérarchique.

|**Structure de niveau supérieur du modèle d'objet Aspose.Diagram**|
|:- |
|![Structure de niveau supérieur du modèle d'objet Aspose.Diagram](diagram-classes.png)|

Comme vous pouvez le voir sur la figure ci-dessus, la racine du modèle d'objet est l'objet Diagram. Une brève description de quelques-uns des objets est fournie ci-dessous à des fins d'introduction.

#### **PageCollection/Page**

L'objet Diagram contient la PageCollection, qui représente la collection de tous les objets Page dans un Diagram.

#### **FormeCollection/Forme**

L'objet Page contient le ShapeCollection, qui représente la collection de tous les objets Shape d'un Page . L'objet Shape contient des éléments qui définissent une forme dans un élément de forme de masque, de page ou de groupe.

#### **ConnectCollection/Connect**

L'objet Page contient la ConnectCollection, qui représente la collection de tous les objets Connect dans un Page . L'objet Connect représente une connexion entre deux formes dans un dessin, comme une ligne et une boîte dans un organigramme.

#### **StyleSheetCollection/StyleSheet**

Représente un style défini dans un document.

#### **MasterCollection/Master**

Contient des éléments qui définissent un masque pour le document. Une forme de base est une forme sur un gabarit que vous utilisez à plusieurs reprises pour créer des dessins. Lorsque vous faites glisser une forme d'un gabarit vers la page de dessin, la forme devient une instance de cette forme de base et une copie locale de la forme de base est incluse dans le document.

#### **Propriétés du document**

Contient des éléments de propriété de document tels que le titre du document, l'auteur, etc.

#### **En-têtePied de page**

Contient des éléments pour l'en-tête et le pied de page d'un document.

#### **Projet Vba**

Représente le projet VBA.

#### **ThèmeCollection/Thème**

Le thème dynamique définit les propriétés qui spécifient les propriétés de couleur, de police, de remplissage, de propriétés de ligne et d'effet.

#### **Remplir**

Contient les valeurs de mise en forme de remplissage actuelles pour la forme et l'ombre portée de la forme, y compris le motif, la couleur de premier plan et la couleur d'arrière-plan.

#### **Ligne**

Contient des éléments qui contrôlent les attributs de ligne d'une forme, tels que le motif, l'épaisseur et la couleur. Ces éléments déterminent si les extrémités de ligne sont formatées (par exemple, avec une pointe de flèche), la taille des formats d'extrémité de ligne, le rayon du cercle d'arrondi appliqué à la ligne et le style de fin de ligne (rond ou carré).

#### **Géomes**

Contient une collection d'éléments Geom.

#### **Caractères**

Contient une collection d'objets Char qui contient les styles de texte de la forme.

#### **Texte**

Contient le texte d'une forme.

#### **XForm**

Contient des éléments spécifiant des informations de positionnement générales sur une forme.

#### **TextXForm**

Contient des éléments qui spécifient des informations de positionnement sur le bloc de texte d'une forme.

#### **Collection de liens hypertexte/lien hypertexte**

L'objet lien hypertexte contient des éléments permettant de créer plusieurs sauts entre une forme ou une page de dessin et une autre page de dessin, un autre fichier ou un site Web.

#### **Forme principale**

Cet attribut ne peut être présent que dans les formes membres d'une forme de groupe, et le groupe est une instance d'une forme de base. L'attribut contient un ID qui fait référence à la sous-forme correspondante dans le masque.

#### **ChampCollection/Champ**

L'objet champ contient des éléments qui spécifient des fonctions et des formules insérées dans le texte de la forme.
