---
title: Travailler avec la protection
type: docs
weight: 90
url: /fr/java/working-with-protection/
---
## **Set Protection du Visio Diagram**
 La protection des diagrammes permet aux utilisateurs de verrouiller les arrière-plans, les masques (gabarits), les formes et les styles afin qu'ils ne puissent pas être modifiés. Ceci est utile pour protéger les styles d'entreprise, par exemple, et assurer une apparence cohérente sur un ensemble de diagrammes. Les développeurs peuvent y parvenir en utilisant[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).
### **Modifier la protection du Visio Diagram**
 Les méthodes getProtectBkgnds, getProtectMasters, getProtectShapes et getProtectStyles, exposées par le[Paramètres du document](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentSettings) prend en charge l'objet com.aspose.diagram.BoolValue. Ces propriétés peuvent être utilisées pour protéger et déprotéger les diagrammes Microsoft Visio.

Au Microsoft Visio vous protégez les documents de cette manière :

1. Ouvrez un diagram au Microsoft Visio.
1. Ouvrez la fenêtre de l'explorateur de dessins.
1.  Faites un clic droit sur un diagram et sélectionnez**Protéger le document** du menu.
1. Dans la fenêtre Protéger le document, cochez ou décochez les options pour verrouiller ou déverrouiller différents éléments diagram.
1.  Cliquez sur**D'ACCORD**.

**Veuillez voir comment nous pouvons vérifier ou effacer les options manuellement.** 

![tâche : image_autre_texte](working-with-protection_1.png)

Utilisez le code ci-dessous dans une application Java pour effectuer les mêmes tâches - verrouiller et déverrouiller différents éléments de votre diagram - en utilisant Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Protection-VisioDiagramProtection-VisioDiagramProtection.java" >}}
### **Modifier la protection de forme Visio**
 La protection des formes Visio permet aux utilisateurs de verrouiller des aspects spécifiques des formes. Les aspects des formes qui peuvent être verrouillés via la protection de forme incluent la largeur, la hauteur, la position x, la position y, la rotation et plus encore. Les développeurs peuvent y parvenir en utilisant[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

 La**getLockAspect()**, **getLockBegin()**, **getLockCalcWH()**, **getLockCrop()**, **getLockCustProp()**, **getLockDelete()**, **getLockEnd()**, **getLockFormat()**, **getLockFromGroupFormat()**, **getLockGroup()**, **getLockHeight()**, **getLockMoveX()**, **getLockMoveY()**, **getLockRotate()**, **getLockSelect()**, **getLockTextEdit()**, **getLockThemeColors()**, **getLockThemeEffects()**, **getLockVtxEdit()** et**getLockWidth()** méthodes exposées par le[protection](https://reference.aspose.com/diagram/java/com.aspose.diagram/Protection) prend en charge l'objet com.aspose.diagram.BoolValue. Ces méthodes peuvent être utilisées pour protéger/déprotéger des formes.

Dans Visio, vous devez effectuer les actions suivantes pour protéger n'importe quelle forme :

1. Ouvrez un diagram au Microsoft Visio.
1. Sélectionnez une forme.
1.  Sélectionner**protection** du**Format** menu (Visio 2007), ou sélectionnez**protection** du**Développeur** menus (Visio 2010).
1.  Dans le**protection** fenêtre, sélectionnez ou désélectionnez les options pour verrouiller ou déverrouiller l'attribut de forme.
1.  Cliquez sur**D'ACCORD**.

**Les options de protection d'une forme, comme on le voit dans Microsoft Visio** 

![tâche : image_autre_texte](working-with-protection_2.png)

Utilisez le code suivant dans votre application Java pour faire la même chose (verrouiller/déverrouiller n'importe quel attribut de forme) en utilisant Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Protection-VisioShapeProtection-VisioShapeProtection.java" >}}
