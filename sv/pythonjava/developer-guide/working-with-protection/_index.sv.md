---
title: Arbeta med skydd
type: docs
weight: 90
url: /sv/python-java/working-with-protection/
---
## **Ställ in skydd för Visio Diagram**
Skydda diagram tillåter användare att låsa bakgrunder, master (stenciler), former och stilar så att de inte kan redigeras. Detta är användbart för att skydda företagsstilar, till exempel, och säkerställa ett konsekvent utseende över en uppsättning diagram. Utvecklare kan uppnå detta med Aspose.Diagram för Python via Java.

### **Redigera skydd av Visio Diagram**
Metoderna getProtectBkgnds, getProtectMasters, getProtectShapes och getProtectStyles, exponerade av klassen DocumentSettings stöder BoolValue-objektet. Dessa egenskaper kan användas för att skydda och avskydda Microsoft Visio diagram.

I Microsoft Visio skyddar du dokument på detta sätt:

1. Öppna ett diagram i Microsoft Visio.
1. Öppna Ritningsutforskarens fönster.
1.  Högerklicka på en diagram och välj**Skydda dokument** från menyn.
1. I fönstret Skydda dokument markerar eller avmarkerar du alternativen för att låsa eller låsa upp olika diagram-element.
1.  Klick**OK**.

**Se hur vi kan kontrollera eller rensa alternativ manuellt.** 

Använd koden nedan i din ansökan för att utföra samma uppgifter – låsa och låsa upp olika delar av din diagram – med Aspose.Diagram för Python via Java.

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

diagram.getDocumentSettings().setProtectBkgnds(BOOL.TRUE)
diagram.getDocumentSettings().setProtectMasters(BOOL.TRUE)
diagram.getDocumentSettings().setProtectShapes(BOOL.TRUE)
diagram.getDocumentSettings().setProtectStyles(BOOL.TRUE)

# save diagram
diagram.save("VisioDiagramProtection_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}
```

### **Redigera Visio Shape Protection**
Genom att skydda Visio-former kan användare låsa specifika aspekter av former. Aspekter av former som kan låsas genom formskydd inkluderar bredd, höjd, x-position, y-position, rotation med mera. Utvecklare kan uppnå detta med Aspose.Diagram för Python via Java.

 De**getLockAspect()**, **getLockBegin()**, **getLockCalcWH()**, **getLockCrop()**, **getLockCustProp()**, **getLockDelete()**, **getLockEnd()**, **getLockFormat()**, **getLockFromGroupFormat()**, **getLockGroup()**, **getLockHeight()**, **getLockMoveX()**, **getLockMoveY()**, **getLockRotate()**, **getLockSelect()**, **getLockTextEdit()**, **getLockThemeColors()**, **getLockThemeEffects()**, **getLockVtxEdit()** och**getLockWidth()** metoder som exponeras av**Skydd** klass stöder BoolValue-objektet. Dessa metoder kan användas för att skydda/avskydda former.

Visio måste du utföra följande åtgärder för att skydda alla former:

1. Öppna ett diagram i Microsoft Visio.
1. Välj en form.
1.  Välj**Skydd** från**Formatera** menyn (Visio 2007), eller välj**Skydd** från**Utvecklaren** meny (Visio 2010).
1.  I den**Skydd** fönster, välj eller rensa alternativ för att låsa eller låsa upp formattribut.
1.  Klick**OK**.

**En forms skyddsalternativ, som ses i Microsoft Visio** 

Använd följande kod i din Java-applikation för att göra samma sak (låsa/låsa upp valfritt formattribut) med Aspose.Diagram för Python via Java.

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
```
