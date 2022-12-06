﻿---
title: Travailler avec la protection
type: docs
weight: 170
url: /fr/net/working-with-protection/
description: Cette section explique comment définir la protection dans le diagram avec Aspose.Diagram.
---
## **Set Protection du Visio Diagram**
 La protection des diagrammes permet aux utilisateurs de verrouiller les arrière-plans, les masques (gabarits), les formes et les styles afin qu'ils ne puissent pas être modifiés. Ceci est utile pour protéger les styles d'entreprise, par exemple, et assurer une apparence cohérente sur un ensemble de diagrammes. Les développeurs peuvent y parvenir en utilisant[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Modifier la protection Visio Diagram**
Les propriétés ProtectBkgnds, ProtectMasters, ProtectShapes et ProtectStyles, exposées par le[Paramètres du document](http://www.aspose.com/api/net/diagram/aspose.diagram/documentsettings) prend en charge l'objet Aspose.Diagram.BoolValue. Ces propriétés peuvent être utilisées pour protéger et déprotéger les diagrammes Microsoft Office Visio. Au Microsoft Visio vous protégez les documents de cette manière :

1. Ouvrez un diagram au Microsoft Visio.
1. Ouvrez la fenêtre de l'explorateur de dessins.
1.  Faites un clic droit sur un diagram et sélectionnez**Protéger le document** du menu.
1. Dans la fenêtre Protéger le document, cochez ou décochez les options pour verrouiller ou déverrouiller différents éléments diagram.
1.  Cliquez sur**D'ACCORD**.
#### **Modifier l'exemple de programmation de protection Diagram**
Utilisez le code ci-dessous dans une application .NET pour effectuer les mêmes tâches comme verrouiller et déverrouiller différents éléments du Visio diagram en utilisant Aspose.Diagram for .NET API.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Protection-VisioDiagramProtection-VisioDiagramProtection.cs" >}}
## **Définir la protection de la forme Visio**
 La protection des formes Visio permet aux utilisateurs de verrouiller des aspects spécifiques des formes. Les aspects des formes qui peuvent être verrouillés via la protection de forme incluent la largeur, la hauteur, la position x, la position y, la rotation et plus encore. Les développeurs peuvent y parvenir en utilisant[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Modifier la protection de forme Visio**
**VerrouillerAspect**, **VerrouillerDébut**, **VerrouillerCalcWH**, **Verrouiller le recadrage**, **LockCustProp**, **VerrouillerSupprimer**, **VerrouillerFin**, **VerrouillerFormat**, **LockFromGroupFormat**, **Groupe de verrouillage**, **VerrouillerHauteur**, **VerrouillerDéplacerX**, **VerrouillerDéplacer**, **VerrouillerRotation**, **VerrouillerSélectionner**, **VerrouillerTexteModifier**, **Verrouiller les couleurs du thème**, **LockThemeEffects**, **LockVtxModifier** et**VerrouillerLargeur** propriétés exposées par[**protection**](http://www.aspose.com/api/net/diagram/aspose.diagram/Protection) soutenir la classe**Aspose.Diagram.BoolValue** objet. Ces propriétés peuvent être utilisées pour protéger et déprotéger des formes.

Dans Microsoft Office Visio, l'utilisateur peut effectuer les actions suivantes pour protéger n'importe quelle forme :

- Ouvert diagram au Microsoft Office Visio
- Sélectionnez n'importe quelle forme
- Sélectionnez 'Protection…' dans le menu 'Format' si vous utilisez Visio 2007 ou sélectionnez 'Protection' dans le menu 'Développeur' si vous utilisez Visio 2010
- Dans la fenêtre "Protection", cochez/décochez n'importe quelle zone de texte pour verrouiller ou déverrouiller n'importe quel attribut de forme
- Appuyer sur OK'
### **Modifier l'exemple de programmation de protection de forme**
Utilisez le code suivant dans votre application .NET pour faire la même chose (verrouiller/déverrouiller n'importe quel attribut de forme) en utilisant Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Protection-VisioShapeProtection-VisioShapeProtection.cs" >}}
