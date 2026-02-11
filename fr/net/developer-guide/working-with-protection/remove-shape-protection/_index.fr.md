---
title: Supprimer la protection de forme
type: docs
weight: 20
url: /fr/net/remove-shape-protection/
description: Cette section explique comment supprimer la protection de forme.
---
## **Supprimer la protection de la forme Visio**
 La protection des formes Visio permet aux utilisateurs de verrouiller des aspects spécifiques des formes. Les aspects des formes qui peuvent être verrouillés via la protection de forme incluent la largeur, la hauteur, la position x, la position y, la rotation et plus encore. Les développeurs peuvent y parvenir en utilisant[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Modifier la protection de forme Visio**
**VerrouillerAspect**, **VerrouillerDébut**, **VerrouillerCalcWH**, **Verrouiller le recadrage**, **LockCustProp**, **VerrouillerSupprimer**, **VerrouillerFin**, **VerrouillerFormat**, **LockFromGroupFormat**, **Groupe de verrouillage**, **VerrouillerHauteur**, **VerrouillerDéplacerX**, **VerrouillerDéplacer**, **VerrouillerRotation**, **VerrouillerSélectionner**, **VerrouillerTexteModifier**, **Verrouiller les couleurs du thème**, **LockThemeEffects**, **LockVtxModifier** et**VerrouillerLargeur** propriétés exposées par[**protection**](http://www.aspose.com/api/net/diagram/aspose.diagram/Protection) soutenir la classe**Aspose.Diagram.BoolValue** objet. Ces propriétés peuvent être utilisées pour protéger et déprotéger des formes.

Dans Microsoft Office Visio, l'utilisateur peut effectuer les actions suivantes pour protéger n'importe quelle forme :

- Ouvert diagram au Microsoft Office Visio
- Sélectionnez n'importe quelle forme
- Sélectionnez 'Protection' dans le menu 'Format' si vous utilisez Visio 2007 ou sélectionnez 'Protection' dans le menu 'Développeur' si vous utilisez Visio 2010
- Dans la fenêtre "Protection", décochez n'importe quelle zone de texte pour déverrouiller n'importe quel attribut de forme
- Appuyer sur OK'
### **Supprimer l'exemple de programmation de protection de forme**
Utilisez le code suivant dans votre application .NET pour faire la même chose (déverrouiller n'importe quel attribut de forme) en utilisant Aspose.Diagram for .NET.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Protection();

// Load diagram
Diagram diagram = new Diagram(dataDir + "ProtectAndUnprotect.vsd");
// Get page by name
Page page = diagram.Pages.GetPage("Flow 1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);

// Set protections
shape.Protection.LockAspect.Value = BOOL.False;
shape.Protection.LockBegin.Value = BOOL.False;
shape.Protection.LockCalcWH.Value = BOOL.False;
shape.Protection.LockCrop.Value = BOOL.False;
shape.Protection.LockCustProp.Value = BOOL.False;
shape.Protection.LockDelete.Value = BOOL.False;
shape.Protection.LockEnd.Value = BOOL.False;
shape.Protection.LockFormat.Value = BOOL.False;
shape.Protection.LockFromGroupFormat.Value = BOOL.False;
shape.Protection.LockGroup.Value = BOOL.False;
shape.Protection.LockHeight.Value = BOOL.False;
shape.Protection.LockMoveX.Value = BOOL.False;
shape.Protection.LockMoveY.Value = BOOL.False;
shape.Protection.LockRotate.Value = BOOL.False;
shape.Protection.LockSelect.Value = BOOL.False;
shape.Protection.LockTextEdit.Value = BOOL.False;
shape.Protection.LockThemeColors.Value = BOOL.False;
shape.Protection.LockThemeEffects.Value = BOOL.False;
shape.Protection.LockVtxEdit.Value = BOOL.False;
shape.Protection.LockWidth.Value = BOOL.False;
            
// Save diagram
diagram.Save(dataDir + "RemoveShapeProtection_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

