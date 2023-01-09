---
title: Travailler avec des calques
type: docs
weight: 130
url: /fr/net/working-with-layers/
description: Cette section explique comment ajouter ou obtenir des informations de calque dans une forme visio avec Aspose.Diagram.
---
## **Configurer des objets de forme avec des calques dans Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) permet de configurer des objets de forme avec des calques dans Microsoft Office Visio diagram. Chaque forme peut appartenir à plusieurs calques afin que les développeurs puissent gérer les formes en fonction des besoins de l'utilisateur final. La[Forme](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) L'objet de classe offre la propriété LayerMember qui permet d'ajouter et de supprimer des objets de forme vers et depuis les calques dans le dessin Visio. Les utilisateurs peuvent gérer ces propriétés par programmation en utilisant Aspose.Diagram API comme suit :
### **Configurer l'exemple de programmation d'objets de forme**
Le morceau de code suivant permet d'ajouter, de supprimer et de déplacer des propriétés d'objet de forme.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Layers-ConfigureShapeLayers-ConfigureShapeLayers.cs" >}}
## **Ajouter un nouveau calque dans le Visio Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) permet aux développeurs d'ajouter de nouveaux calques pour organiser des catégories personnalisées de formes, puis d'attribuer des formes à ces calques par programmation. La[LayerCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) la classe propose la méthode Add qui permet d'ajouter un nouveau[Couche](http://www.aspose.com/api/net/diagram/aspose.diagram/layer) dans le dessin Visio. Les développeurs peuvent définir les propriétés de la couche en initialisant son objet de classe.
### **Ajouter un exemple de programmation de couche**
Le morceau de code suivant permet d'ajouter des objets Layer.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Layers-AddLayer-AddLayer.cs" >}}
## **Récupérer toutes les couches du Visio Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) donne accès aux développeurs pour obtenir les couches existantes d'un Visio diagram. Le[Feuille de page](http://www.aspose.com/api/net/diagram/aspose.diagram/pagesheet) propriété de la[Page](http://www.aspose.com/api/net/diagram/aspose.diagram/page) class permet de récupérer la liste des couches disponibles à partir d'un Visio diagram en utilisant[LayerCollection](http://www.aspose.com/api/net/diagram/aspose.diagram/layercollection) classer.
### **Récupérer un exemple de programmation de calques**
Le morceau de code suivant aide à obtenir la liste des couches.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Layers-RetrieveAllLayers-RetrieveAllLayers.cs" >}}
