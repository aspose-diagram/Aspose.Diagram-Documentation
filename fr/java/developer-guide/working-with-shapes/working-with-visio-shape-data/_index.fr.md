---
title: Utilisation des données de forme Visio
type: docs
weight: 30
url: /fr/java/working-with-visio-shape-data/
---
## **Ajout d'une nouvelle forme dans Visio**
Aspose.Diagram for Java vous permet de manipuler les diagrammes Microsoft Visio de différentes manières. L'une des choses que vous pouvez faire est d'ajouter de nouvelles formes à un diagramme. Aspose.Diagram for Java vous permet d'ajouter une nouvelle forme à un diagram. La forme ajoutée peut également être personnalisée à l'aide de Aspose.Diagram for Java.

Cette rubrique décrit comment ajouter une nouvelle forme de rectangle à un diagram.

Utilisez le API de Aspose.Diagram for Java pour créer de nouvelles formes, puis ajoutez ces formes à une collection de formes de diagram.

Pour ajouter une nouvelle forme :

1. **Trouver la page** - Chaque Visio diagram contient une collection de pages. Les développeurs peuvent récupérer la page par ID de page ou nom et stocker la page requise dans le[Page](https://reference.aspose.com/diagram//java/com.aspose.diagram/page)objet de classe.
1. **Ajouter le maître requis d'une forme** - Chaque Visio diagram contient une collection de maîtres. Les développeurs peuvent ajouter un maître (par ID ou nom) à partir du fichier de gabarit existant (par chemin direct ou flux de fichier).
1. **Ajouter une forme dans le Visio diagram** - Les développeurs peuvent placer une nouvelle forme dans le Visio diagram par index de page (à partir de 0), nom principal, PinX, PinY, hauteur (facultatif) et largeur (facultatif).
1. **Définir les propriétés de la forme** - La méthode AddShape de la classe Diagram renvoie l'ID de la forme. Les développeurs peuvent récupérer la forme d'un Visio diagram en utilisant cet ID, puis définir ses propriétés, par exemple la couleur, la position, l'alignement et le texte.

|<p>**L'entrée diagram** </p><p>![tâche : image_autre_texte](working-with-visio-shape-data_1.png)</p>|<p>**Le diagram avec une forme ajoutée** </p><p>![tâche : image_autre_texte](working-with-visio-shape-data_2.png)</p>|
|:- |:- |
### **Ajouter un échantillon de programmation**
L'extrait de code ci-dessous montre comment effectuer chaque étape.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-AddingNewShape-AddingNewShape.java" >}}

{{% alert color="primary" %}}

 Nous accueillons vos questions et suggestions à[Aspose.DiagramForum](https://forum.aspose.com/c/diagram/17). Nous vous répondrons rapidement.

{{% /alert %}}
## **Récupération des informations sur la forme**
[Travailler avec des diagrammes](/diagram/fr/java/working-with-diagrams/)explique comment créer des diagrammes, ajouter des formes et des connecteurs, puis comment récupérer des informations sur les éléments diagram tels que[pages](/diagram/fr/java/retrieve-get-copy-and-insert-a-page/), [maîtrise](/diagram/fr/java/working-with-masters/) , connecteurs et[polices](/diagram/fr/java/aspose-diagram-font-operations/). Cet article explique comment récupérer des informations sur les formes dans un fichier diagram.

Chaque forme dans un diagram a un ID et un nom. L'ID est important lors de la programmation avec Visio : c'est la principale méthode d'accès à une forme. Chaque forme conserve également des informations sur le maître (pochoir) à partir duquel elle est fabriquée.

 UN[Forme](https://reference.aspose.com/diagram//java/com.aspose.diagram/shape) est un objet dans un dessin Visio. La propriété Shapes, exposée par la classe Page, prend en charge une collection d'objets Aspose.Diagram.Shape. La propriété Shapes peut être utilisée pour récupérer des informations sur une forme.

Dans la fenêtre de console ci-dessous, par exemple, vous pouvez voir la sortie d'informations pour un diagram qui contenait quatre formes : deux terminateurs, un processus et un connecteur dynamique. Chacun a un identifiant unique ainsi que le nom de la forme principale (pochoir).

**Une fenêtre de console affichant des informations sur la forme**

![tâche : image_autre_texte](working-with-visio-shape-data_3.png)

Pour récupérer les informations de la page Visio :

1. Charge un diagram.
1. Configure une boucle foreach pour parcourir toutes les formes du diagram.
1. Affiche les informations sur la forme.
### **Récupérer l'exemple de programmation**
Le morceau de code suivant récupère les informations de forme à partir d'un Visio diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveShapeInfo-RetrieveShapeInfo.java" >}}
## **Copier des formes à partir d'un Visio existant**
Aspose.Diagram for Java API permet aux développeurs de copier des formes de la page source Visio vers la nouvelle page Visio diagram. Il prend également en charge la copie de formes de groupe. Cet article décrit comment copier toutes les formes à partir de la page source diagram.

Pour copier des formes, les développeurs doivent également copier les thèmes source PageSheet et source Visio afin de préserver le style de remplissage de la forme et d'autres propriétés de mise en forme.

Cet exemple fonctionne comme suit :

1. Charger une source Visio.
1. Initialiser un nouveau Visio
1. Ajoutez des masters et des thèmes à partir de la source Visio.
1. Obtenir la page de la source Visio.
1. Copiez sa feuille de page sur la nouvelle page Visio.
1. Parcourez les formes de la page source Visio.
1. Définissez son nouvel identifiant et ajoutez-le à la nouvelle page Visio.
1. Enregistrez le nouveau Visio dans le stockage local.
### **Copier l'exemple de programmation**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-CopyShape-CopyShape.java" >}}

{{% alert color="primary" %}}

 Nous accueillons vos questions et suggestions à[Aspose.DiagramForum](https://forum.aspose.com/c/diagram/17). Nous vous répondrons rapidement.

{{% /alert %}}
## **Copier une forme Visio dans une autre instance de forme**
La méthode de copie de la classe Shape prend une instance de forme à cloner.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Shape newShape = new Shape();

// copy diagram

newShape.copy(diagram.getPages().get(0).getShapes().get(0));

newShape.setID(3);

newShape.getXForm().getPinX().setValue(1);

newShape.getXForm().getPinY().setValue(1);

{{< /highlight >}}
## **Lecture des données de forme Visio**
 La collection Props exposée par la classe Shape prend en charge la[Aspose.Diagram.Prop](https://reference.aspose.com/diagram//java/com.aspose.diagram/prop) objet. La propriété peut être utilisée pour lire les données d'une forme (propriétés personnalisées).
### **Lire toutes les propriétés de forme**
Pour identifier les propriétés personnalisées dans Microsoft Visio :

1. Dans un diagram, cliquez avec le bouton droit sur une forme.
1.  Sélectionner**Données** , alors**Données de forme** du menu.
 Toutes les propriétés existantes sont répertoriées dans la boîte de dialogue.

|**Les données d'une forme, comme dans Microsoft Visio.**|** |
|:- |:- |
|![tâche : image_autre_texte](http://i.imgur.com/2loM7b0.png)||


|**Une fenêtre de console affichant la sortie des données de forme.**|** |
|:- |:- |
|![tâche : image_autre_texte](http://i.imgur.com/kmAKNrx.png)||
#### **Lire l'exemple de programmation**
Les extraits de code ci-dessous lisent les données de forme (propriétés personnalisées).

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ReadAllShapeProps-ReadAllShapeProps.java" >}}
### **Lire une propriété de forme par nom**
L'extrait de code ci-dessous lit une propriété de forme par son nom (propriété personnalisée).
#### **Exemple de programmation de lecture par nom**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ReadShapePropByName-ReadShapePropByName.java" >}}
## **Utiliser les index de connexion pour connecter des formes**
Aspose.Diagram for Java API permet déjà aux développeurs d'ajouter de nouveaux points de connexion sur la forme, et les développeurs peuvent désormais connecter des formes à l'aide d'index de connexion.
### **Utiliser les index de connexion pour connecter des formes**
Le membre connectShapesViaConnectorIndex exposé par la classe Page peut être utilisé pour connecter des formes à l'aide d'index de connexion. Le code suivant montre comment connecter des formes :

1. Initialiser un nouveau dessin.
1. Placez quatre formes rectangulaires
1. Ajoutez deux points de connexion supplémentaires, de sorte qu'il y aurait trois points de connexion sur la ligne de bordure inférieure
1. Connectez la première forme de chaque connexion inférieure aux trois autres formes rectangulaires du haut avec des connecteurs dynamiques
1. Enregistrer le dessin
#### **Utiliser des index de connexion pour connecter des formes Exemple de programmation**
Utilisez le code suivant dans votre application Java pour connecter des formes à l'aide d'index de connexion avec Aspose.Diagram for Java API.

**Java**

{{< highlight "java" >}}

 // initialize a new drawing

Diagram diagram = new Diagram();

// get page by index

Page page = diagram.getPages().get(0);

// add masters

String connectorMaster = "Dynamic connector", rectangle = "Rectangle";

int pageNumber = 0;

double width = 2, height = 2, pinX = 4.25, pinY = 9.5;

diagram.addMaster("C:\\temp\\Basic Shapes.vss", rectangle);

diagram.addMaster("C:\\temp\\Basic Shapes.vss", connectorMaster);

// add shapes

long shape1_ID = diagram.addShape(4.5, 7, rectangle, pageNumber);

long shape2_ID = diagram.addShape(2.25, 4.5, rectangle, pageNumber);

long shape3_ID = diagram.addShape(4.5, 4.5, rectangle, pageNumber);

long shape4_ID = diagram.addShape(6.75, 4.5, rectangle, pageNumber);

// get shapes by ID

Shape shape1 = page.getShapes().getShape(shape1_ID);

Shape shape2 = page.getShapes().getShape(shape2_ID);

Shape shape3 = page.getShapes().getShape(shape3_ID);

Shape shape4 = page.getShapes().getShape(shape4_ID);

// add two more connection points

Connection connection1 = new Connection();

connection1.getX().getUfe().setF("Width*0.33");

connection1.getY().getUfe().setF("Height*0");

Connection connection3 = new Connection();

connection3.getX().getUfe().setF("Width*0.66");

connection3.getY().getUfe().setF("Height*0");

shape1.getConnections().add(connection1);

shape1.getConnections().add(connection3);



// add connector shapes

Shape connector1 = new Shape();

Shape connector2 = new Shape();

Shape connector3 = new Shape();

long connecter1Id = diagram.addShape(connector1, connectorMaster, 0);

long connecter2Id = diagram.addShape(connector2, connectorMaster, 0);

long connecter3Id = diagram.addShape(connector3, connectorMaster, 0);

// connect shapes by index of conneecting points

page.connectShapesViaConnectorIndex(shape1.getID(), 6, shape2.getID(), 3, connecter1Id);

page.connectShapesViaConnectorIndex(shape1.getID(), 1, shape3.getID(), 3, connecter2Id);

page.connectShapesViaConnectorIndex(shape1.getID(), 7, shape4.getID(), 3, connecter3Id);

// save drawing

diagram.save("C:\\temp\\Drawing1_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
## **Récupérer la forme parent d'une sous-forme**
Aspose.Diagram for Java permet aux développeurs de récupérer la forme parent d'une sous-forme.
### **Obtenir la forme parent**
La classe Shape propose la propriété getParentShape pour récupérer la forme parent.
#### **Obtenir l'exemple de programmation de la forme parent**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-RetrieveTheParentShape-RetrieveTheParentShape.java" >}}
