---
title: Supprimer la protection de forme
type: docs
weight: 20
url: /fr/python-java/remove-shape-protection/
description: This section explains how to remove shape protection using Aspose.Diagram for Python via Java.
---
## **Supprimer la protection de la forme Visio**
Protecting Visio shapes allow users to lock specific aspects of shapes. Aspects of shapes that can be locked through shape protection include width, height, x-position, y-position, rotation and more. Developers can achieve this using Aspose.Diagram for Python via Java.
### **Modifier la protection de forme Visio**
**VerrouillerAspect**, **VerrouillerDébut**, **VerrouillerCalcWH**, **Verrouiller le recadrage**, **LockCustProp**, **VerrouillerSupprimer**, **VerrouillerFin**, **VerrouillerFormat**, **LockFromGroupFormat**, **Groupe de verrouillage**, **VerrouillerHauteur**, **VerrouillerDéplacerX**, **VerrouillerDéplacer**, **VerrouillerRotation**, **VerrouillerSélectionner**, **VerrouillerTexteModifier**, **Verrouiller les couleurs du thème**, **LockThemeEffects**, **LockVtxModifier** et**VerrouillerLargeur** propriétés exposées par**protection** soutenir la classe**Aspose.Diagram.BoolValue** objet. Ces propriétés peuvent être utilisées pour protéger et déprotéger des formes.

Dans Microsoft Office Visio, l'utilisateur peut effectuer les actions suivantes pour protéger n'importe quelle forme :

- Ouvert diagram au Microsoft Office Visio
- Sélectionnez n'importe quelle forme
- Sélectionnez 'Protection' dans le menu 'Format' si vous utilisez Visio 2007 ou sélectionnez 'Protection' dans le menu 'Développeur' si vous utilisez Visio 2010
- Dans la fenêtre "Protection", décochez n'importe quelle zone de texte pour déverrouiller n'importe quel attribut de forme
- Appuyer sur OK'

### **Supprimer l'exemple de programmation de protection de forme**
Use the following code in your application to do the same thing (unlock any shape attribute) using Aspose.Diagram for Python via Java.

```
{{< highlight "python" >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Load diagram
diagram = Diagram("ProtectAndUnprotect.vsd")
# get page by name
page = diagram.getPages().getPage("Flow 1")
# get shape by ID
shape = page.getShapes().getShape(1)

# set protections
shape.getProtection().getLockAspect().setValue(BOOL.FALSE)
shape.getProtection().getLockBegin().setValue(BOOL.FALSE)
shape.getProtection().getLockCalcWH().setValue(BOOL.FALSE)
shape.getProtection().getLockCrop().setValue(BOOL.FALSE)
shape.getProtection().getLockCustProp().setValue(BOOL.FALSE)
shape.getProtection().getLockDelete().setValue(BOOL.FALSE)
shape.getProtection().getLockEnd().setValue(BOOL.FALSE)
shape.getProtection().getLockFormat().setValue(BOOL.FALSE)
shape.getProtection().getLockFromGroupFormat().setValue(BOOL.FALSE)
shape.getProtection().getLockGroup().setValue(BOOL.FALSE)
shape.getProtection().getLockHeight().setValue(BOOL.FALSE)
shape.getProtection().getLockMoveX().setValue(BOOL.FALSE)
shape.getProtection().getLockMoveY().setValue(BOOL.FALSE)
shape.getProtection().getLockRotate().setValue(BOOL.FALSE)
shape.getProtection().getLockSelect().setValue(BOOL.FALSE)
shape.getProtection().getLockTextEdit().setValue(BOOL.FALSE)
shape.getProtection().getLockThemeColors().setValue(BOOL.FALSE)
shape.getProtection().getLockThemeEffects().setValue(BOOL.FALSE)
shape.getProtection().getLockVtxEdit().setValue(BOOL.FALSE)
shape.getProtection().getLockWidth().setValue(BOOL.FALSE)
        
# save diagram
diagram.save("VisioShapeProtection_Out.vsdx", SaveFileFormat.VSDX)
jpype.shutdownJVM()

{{< /highlight >}}
```

