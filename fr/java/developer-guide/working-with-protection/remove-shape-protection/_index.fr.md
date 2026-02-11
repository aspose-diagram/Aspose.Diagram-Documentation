---
title: Supprimer la protection de forme
type: docs
weight: 20
url: /fr/java/remove-shape-protection/
description: Cette section explique comment supprimer la protection de forme à l'aide du Aspose.Diagram.
---
## **Supprimer la protection de la forme Visio**
 La protection des formes Visio permet aux utilisateurs de verrouiller des aspects spécifiques des formes. Les aspects des formes qui peuvent être verrouillés via la protection de forme incluent la largeur, la hauteur, la position x, la position y, la rotation et plus encore. Les développeurs peuvent y parvenir en utilisant[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).
### **Modifier la protection de forme Visio**
**VerrouillerAspect**, **VerrouillerDébut**, **VerrouillerCalcWH**, **Verrouiller le recadrage**, **LockCustProp**, **VerrouillerSupprimer**, **VerrouillerFin**, **VerrouillerFormat**, **LockFromGroupFormat**, **Groupe de verrouillage**, **VerrouillerHauteur**, **VerrouillerDéplacerX**, **VerrouillerDéplacer**, **VerrouillerRotation**, **VerrouillerSélectionner**, **VerrouillerTexteModifier**, **Verrouiller les couleurs du thème**, **LockThemeEffects**, **LockVtxModifier** et**VerrouillerLargeur** propriétés exposées par[**protection**](https://reference.aspose.com/diagram/java/com.aspose.diagram/protection) soutenir la classe**Aspose.Diagram.BoolValue** objet. Ces propriétés peuvent être utilisées pour protéger et déprotéger des formes.

Dans Microsoft Office Visio, l'utilisateur peut effectuer les actions suivantes pour protéger n'importe quelle forme :

- Ouvert diagram au Microsoft Office Visio
- Sélectionnez n'importe quelle forme
- Sélectionnez 'Protection' dans le menu 'Format' si vous utilisez Visio 2007 ou sélectionnez 'Protection' dans le menu 'Développeur' si vous utilisez Visio 2010
- Dans la fenêtre "Protection", décochez n'importe quelle zone de texte pour déverrouiller n'importe quel attribut de forme
- Appuyer sur OK'
### **Supprimer l'exemple de programmation de protection de forme**
Utilisez le code suivant dans votre application Java pour faire la même chose (déverrouiller n'importe quel attribut de forme) en utilisant Aspose.Diagram for Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VisioShapeProtection.class);
//Load diagram
Diagram diagram = new Diagram(dataDir + "ProtectAndUnprotect.vsd");
// get page by name
Page page = diagram.getPages().getPage("Flow 1");
// get shape by ID
Shape shape = page.getShapes().getShape(1);

// set protections
shape.getProtection().getLockAspect().setValue(BOOL.FALSE);
shape.getProtection().getLockBegin().setValue(BOOL.FALSE);
shape.getProtection().getLockCalcWH().setValue(BOOL.FALSE);
shape.getProtection().getLockCrop().setValue(BOOL.FALSE);
shape.getProtection().getLockCustProp().setValue(BOOL.FALSE);
shape.getProtection().getLockDelete().setValue(BOOL.FALSE);
shape.getProtection().getLockEnd().setValue(BOOL.FALSE);
shape.getProtection().getLockFormat().setValue(BOOL.FALSE);
shape.getProtection().getLockFromGroupFormat().setValue(BOOL.FALSE);
shape.getProtection().getLockGroup().setValue(BOOL.FALSE);
shape.getProtection().getLockHeight().setValue(BOOL.FALSE);
shape.getProtection().getLockMoveX().setValue(BOOL.FALSE);
shape.getProtection().getLockMoveY().setValue(BOOL.FALSE);
shape.getProtection().getLockRotate().setValue(BOOL.FALSE);
shape.getProtection().getLockSelect().setValue(BOOL.FALSE);
shape.getProtection().getLockTextEdit().setValue(BOOL.FALSE);
shape.getProtection().getLockThemeColors().setValue(BOOL.FALSE);
shape.getProtection().getLockThemeEffects().setValue(BOOL.FALSE);
shape.getProtection().getLockVtxEdit().setValue(BOOL.FALSE);
shape.getProtection().getLockWidth().setValue(BOOL.FALSE);
        
// save diagram
diagram.save(dataDir + "VisioShapeProtection_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

