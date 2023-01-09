---
title: Protéger les formes dans Visio
type: docs
weight: 20
url: /fr/net/protect-shapes-in-visio/
---
LockAspect, LockBegin, LockCalcWH, LockCrop, LockCustProp, LockDelete, LockEnd, LockFormat, LockFromGroupFormat, LockGroup, LockHeight, LockMoveX, LockMoveY, LockRotate, LockSelect, LockTextEdit, LockThemeColors, LockThemeEffects, LockVtxEdit et LockWidth exposés par la classe Protection prennent en charge l'objet Aspose.Diagram.BoolValue . Ces propriétés peuvent être utilisées pour protéger/déprotéger des formes.

Dans Visio, vous devez effectuer les actions suivantes pour protéger n'importe quelle forme :

- Ouvrez diagram dans MS Visio
- Sélectionnez n'importe quelle forme
- Sélectionnez 'Protection…' dans le menu 'Format' si vous utilisez Visio 2007 ou sélectionnez 'Protection' dans le menu 'Développeur' si vous utilisez Visio 2010
- Dans la fenêtre "Protection", cochez/décochez n'importe quelle zone de texte pour verrouiller ou déverrouiller n'importe quel attribut de forme
- Appuyer sur OK'

Utilisez le code suivant dans votre application .NET pour faire la même chose (verrouiller n'importe quel attribut de forme) en utilisant Aspose.Diagram for .NET.

{{< highlight "csharp" >}}

 //Load diagram

Diagram diagram = new Diagram("ProtectShape.vsd");

Page page0 = diagram.Pages[0];

Shape shape = page0.Shapes[0];

shape.Protection.LockAspect.Value = BOOL.True;

shape.Protection.LockBegin.Value = BOOL.True;

shape.Protection.LockCalcWH.Value = BOOL.True;

shape.Protection.LockCrop.Value = BOOL.True;

shape.Protection.LockCustProp.Value = BOOL.True;

shape.Protection.LockDelete.Value = BOOL.True;

shape.Protection.LockEnd.Value = BOOL.True;

shape.Protection.LockFormat.Value = BOOL.True;

shape.Protection.LockFromGroupFormat.Value = BOOL.True;

shape.Protection.LockGroup.Value = BOOL.True;

shape.Protection.LockHeight.Value = BOOL.True;

shape.Protection.LockMoveX.Value = BOOL.True;

shape.Protection.LockMoveY.Value = BOOL.True;

shape.Protection.LockRotate.Value = BOOL.True;

shape.Protection.LockSelect.Value = BOOL.True;

shape.Protection.LockTextEdit.Value = BOOL.True;

shape.Protection.LockThemeColors.Value = BOOL.True;

shape.Protection.LockThemeEffects.Value = BOOL.True;

shape.Protection.LockVtxEdit.Value = BOOL.True;

shape.Protection.LockWidth.Value = BOOL.True;

diagram.Save("ProtectedShapesFile.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
## **Télécharger l'exemple de code**
- [Bitbucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/src/master/Aspose.Diagram%20Vs%20VSTO%20Visio/)
