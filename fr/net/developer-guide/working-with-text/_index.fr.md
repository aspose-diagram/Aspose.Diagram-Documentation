---
title: Travailler avec du texte
type: docs
weight: 90
url: /fr/net/working-with-text/
description: Cette section explique comment insérer une forme de texte ou mettre à jour le texte de la forme avec Aspose.Diagram.
---
## **Insérer une forme de texte dans la page Visio**
 Aspose.Diagram API permet aux développeurs d'insérer une forme de texte n'importe où dans la page Visio. Pour ce faire, la méthode AddText de la[Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) La classe prend les paramètres PinX, PinY, largeur, hauteur et texte.
### **Insérer un exemple de programmation de forme de texte**
Le morceau de code suivant ajoute une forme de texte dans le Visio diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-InsertTextShape-InsertTextShape.cs" >}}
## **Mise à jour Visio Texte de forme**
 Aussi bien que[création de diagrammes](/diagram/fr/net/load-or-create-a-visio-drawing/) , Aspose.Diagram for .NET vous permet de travailler avec des formes de différentes manières. Cet article explique comment accéder au texte et le mettre à jour dans les formes. La propriété Text, exposée par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) classe, prend en charge l'objet Aspose.Diagram.Text. La propriété peut être utilisée pour récupérer ou mettre à jour le texte d'une forme. Le processus de mise à jour du texte d'une forme est simple :

1. Charger un diagram.
1. Trouvez une forme particulière.
1. Définissez le nouveau texte.
1. Enregistrez le diagram.
### **Mise à jour de l'exemple de programmation de texte de forme**
Le morceau de code suivant met à jour le texte d'une forme. Les formes sont identifiées par leurs identifiants. Les segments de code ci-dessous recherchent une forme appelée processus et avec l'ID 1 et modifient son texte.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-UpdateShapeText-UpdateShapeText.cs" >}}
## **Appliquer une feuille de style intégrée ou personnalisée à une forme Visio**
Les feuilles de style Microsoft Visio stockent les informations de mise en forme qui peuvent être appliquées aux formes pour une apparence cohérente. Aspose.Diagram for .NET vous permet d'appliquer des feuilles de style depuis l'intérieur d'une application.

 Les propriétés TextStyle, FillStyle et LineStyle exposées par le[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) soutenir la classe[Aspose.Diagram.StyleSheet](http://www.aspose.com/api/net/diagram/aspose.diagram/stylesheet) objet. La propriété peut être utilisée pour récupérer des informations de style et appliquer des styles de texte, de ligne et de remplissage personnalisés à un diagram.
### **Styles personnalisés dans Microsoft Visio**
Pour appliquer des styles personnalisés aux formes dans Microsoft Visio :

1. Ouvrez un diagram au Microsoft Visio.
1.  Sélectionner**Définir les styles** du**Format** menu (Visio 2007), ou clic droit**modes** dans le**Explorateur de dessins** fenêtre et sélectionnez**Définir les styles** (Visio 2010).
1.  Dans le**Définir les styles** boîte de dialogue, saisissez un nouveau nom pour votre feuille de style personnalisée. Par exemple, CustomStyle1.
1.  Clique le**Texte**, **Ligne** et**Remplir** boutons pour définir respectivement les styles de texte, de ligne et de remplissage.
1.  Cliquez sur**D'ACCORD**.

Après avoir défini des feuilles de style personnalisées dans Microsoft Visio, utilisez le code suivant dans une application .NET pour appliquer des styles personnalisés à vos formes. Notez que les exemples de code ci-dessous appellent la feuille de style personnalisée définie ci-dessus : vous devez connaître le nom et l'emplacement de la feuille que vous appliquez. Pour appliquer des styles personnalisés par programmation :

1. Charger un diagram.
1. Recherchez la forme à laquelle vous souhaitez appliquer un style.
1. Chargez la feuille de style.
1. Appliquer des styles.
1. Enregistrez le diagram.
#### **Appliquer un exemple de programmation de styles personnalisés**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-ApplyCustomStyleSheets-ApplyCustomStyleSheets.cs" >}}
## **Appliquer un style différent sur chaque valeur de texte d'une forme**
 Aussi bien que[création de diagrammes](/diagram/fr/net/load-or-create-a-visio-drawing/), Aspose.Diagram for .NET vous permet de travailler avec des formes de différentes manières. Cet article vous aide à ajouter plusieurs valeurs de texte à une forme et à appliquer un style différent à chaque valeur de texte.

{{% alert color="primary" %}} 

L'élément Shape contient un élément appelé Text, qui contient les caractères du texte et des éléments spéciaux (cp, pp, tp et fld) qui marquent la fin d'une exécution et le début de la suivante. Char Element contient les attributs de mise en forme du texte de la forme, tels que la police, la couleur, le style de texte, la casse, la position par rapport à la ligne de base et la taille en points.

{{% /alert %}} 
### **Ajout de texte et de styles de forme**

|**Entrée diagram**|
|:- |
|![tâche : image_autre_texte](working-with-text_1.png)|


|**Diagram après avoir ajouté diverses valeurs de texte à une forme avec un style différent sur chaque valeur de texte**|
|:- |
|![tâche : image_autre_texte](working-with-text_2.png)|
#### **Exemple de programmation d'ajout de texte et de styles**
Le morceau de code suivant ajoute le texte d'une forme et différents styles.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-ApplyFontOnText-ApplyFontOnText.cs" >}}
## **Rechercher et remplacer le texte d'une forme**
 La[SMS](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) La classe vous permet de modifier le texte de la forme. La méthode Replace, exposée par le[SMS](http://www.aspose.com/api/net/diagram/aspose.diagram/txt) classe, prend en charge la modification du texte d'une forme.
Les exemples de code de cet article recherchent et remplacent le texte de la forme sur la page.

|**Entrée diagram**|
|:- |
|![tâche : image_autre_texte](working-with-text_3.png)|


|**Le diagram après la modification de la forme**|
|:- |
|![tâche : image_autre_texte](working-with-text_4.png)|
Le processus de modification du texte de la forme :

1. Charger un diagram.
1. Trouver un texte particulier d'une forme.
1. Remplacer le texte de cette forme
1. Enregistrez le diagram.
### **Rechercher et remplacer un exemple de programmation de texte**
Les extraits de code ci-dessous montrent comment modifier le texte de la forme. Le code parcourt les formes d'une page.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-FindAndReplaceShapeText-FindAndReplaceShapeText.cs" >}}
## **Extraire le texte brut de la page Visio Diagram**
Aspose.Diagram API permet aux développeurs d'extraire du texte brut de la page Visio diagram. Ils peuvent également parcourir les pages Visio diagram pour couvrir l'ensemble du texte Visio diagram.

 Microsoft Office Visio ajoute le texte aux formes. La[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) La classe contient un élément appelé Text, qui contient les caractères du texte et des éléments spéciaux (cp, pp, tp et fld) qui marquent la fin d'une exécution et le début de la suivante.
### **Extraire un exemple de programmation en texte brut**
Le morceau de code suivant parcourt les formes de la page Visio et filtre le texte brut sans formater les informations.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Text-GetPlainTextOfVisio-GetPlainTextOfVisio.cs" >}}
