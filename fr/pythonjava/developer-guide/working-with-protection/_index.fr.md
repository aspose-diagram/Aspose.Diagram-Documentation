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


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Load diagram
diagram = Diagram("ProtectAndUnprotect.vsd")

diagram.getDocumentSettings().setProtectBkgnds(BOOL.TRUE)
diagram.getDocumentSettings().setProtectMasters(BOOL.TRUE)
diagram.getDocumentSettings().setProtectShapes(BOOL.TRUE)
diagram.getDocumentSettings().setProtectStyles(BOOL.TRUE)

# save diagram
diagram.save("VisioDiagramProtection_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}


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


{{< highlight python >}}
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
shape.getProtection().getLockAspect().setValue(BOOL.TRUE)
shape.getProtection().getLockBegin().setValue(BOOL.TRUE)
shape.getProtection().getLockCalcWH().setValue(BOOL.TRUE)
shape.getProtection().getLockCrop().setValue(BOOL.TRUE)
shape.getProtection().getLockCustProp().setValue(BOOL.TRUE)
shape.getProtection().getLockDelete().setValue(BOOL.TRUE)
shape.getProtection().getLockEnd().setValue(BOOL.TRUE)
shape.getProtection().getLockFormat().setValue(BOOL.TRUE)
shape.getProtection().getLockFromGroupFormat().setValue(BOOL.TRUE)
shape.getProtection().getLockGroup().setValue(BOOL.TRUE)
shape.getProtection().getLockHeight().setValue(BOOL.TRUE)
shape.getProtection().getLockMoveX().setValue(BOOL.TRUE)
shape.getProtection().getLockMoveY().setValue(BOOL.TRUE)
shape.getProtection().getLockRotate().setValue(BOOL.TRUE)
shape.getProtection().getLockSelect().setValue(BOOL.TRUE)
shape.getProtection().getLockTextEdit().setValue(BOOL.TRUE)
shape.getProtection().getLockThemeColors().setValue(BOOL.TRUE)
shape.getProtection().getLockThemeEffects().setValue(BOOL.TRUE)
shape.getProtection().getLockVtxEdit().setValue(BOOL.TRUE)
shape.getProtection().getLockWidth().setValue(BOOL.TRUE)
        
# save diagram
diagram.save("VisioShapeProtection_Out.vdx", SaveFileFormat.VDX)
jpype.shutdownJVM()

{{< /highlight >}}

