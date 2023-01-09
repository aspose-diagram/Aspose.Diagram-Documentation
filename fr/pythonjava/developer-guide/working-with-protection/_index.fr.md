---
title: Travailler avec la protection
type: docs
weight: 90
url: /fr/python-java/working-with-protection/
---
## **Set Protection du Visio Diagram**
Protecting diagrams allow users to lock backgrounds, masters (stencils), shapes and styles so that they cannot be edited. This is useful for protecting corporate styles, for example, and ensure a consistent look across a set of diagrams. Developers can achieve this using Aspose.Diagram for Python via Java.

### **Modifier la protection du Visio Diagram**
Les méthodes getProtectBkgnds, getProtectMasters, getProtectShapes et getProtectStyles, exposées par la classe DocumentSettings prennent en charge l'objet BoolValue. Ces propriétés peuvent être utilisées pour protéger et déprotéger les diagrammes Microsoft Visio.

Au Microsoft Visio vous protégez les documents de cette manière :

1. Ouvrez un diagram au Microsoft Visio.
1. Ouvrez la fenêtre de l'explorateur de dessins.
1.  Faites un clic droit sur un diagram et sélectionnez**Protéger le document** du menu.
1. Dans la fenêtre Protéger le document, cochez ou décochez les options pour verrouiller ou déverrouiller différents éléments diagram.
1.  Cliquez sur**D'ACCORD**.

**Veuillez voir comment nous pouvons vérifier ou effacer les options manuellement.** 

Use the code below in your application to perform the same tasks – lock and unlock different elements of your diagram – using Aspose.Diagram for Python via Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-VisioDiagramProtection.py" >}}

### **Modifier la protection de forme Visio**
Protecting Visio shapes allow users to lock specific aspects of shapes. Aspects of shapes that can be locked through shape protection include width, height, x-position, y-position, rotation and more. Developers can achieve this using Aspose.Diagram for Python via Java.

 La**getLockAspect()**, **getLockBegin()**, **getLockCalcWH()**, **getLockCrop()**, **getLockCustProp()**, **getLockDelete()**, **getLockEnd()**, **getLockFormat()**, **getLockFromGroupFormat()**, **getLockGroup()**, **getLockHeight()**, **getLockMoveX()**, **getLockMoveY()**, **getLockRotate()**, **getLockSelect()**, **getLockTextEdit()**, **getLockThemeColors()**, **getLockThemeEffects()**, **getLockVtxEdit()** et**getLockWidth()** méthodes exposées par le**protection** prend en charge l'objet BoolValue. Ces méthodes peuvent être utilisées pour protéger/déprotéger des formes.

Dans Visio, vous devez effectuer les actions suivantes pour protéger n'importe quelle forme :

1. Ouvrez un diagram au Microsoft Visio.
1. Sélectionnez une forme.
1.  Sélectionner**protection** du**Format** menu (Visio 2007), ou sélectionnez**protection** du**Développeur** menus (Visio 2010).
1.  Dans le**protection** fenêtre, sélectionnez ou désélectionnez les options pour verrouiller ou déverrouiller l'attribut de forme.
1.  Cliquez sur**D'ACCORD**.

**Les options de protection d'une forme, comme on le voit dans Microsoft Visio** 

Use the following code in your Java application to do the same thing (lock/unlock any shape attribute) using Aspose.Diagram for Python via Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-VisioShapeProtection.py" >}}
