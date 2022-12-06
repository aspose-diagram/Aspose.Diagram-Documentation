---
title: Arbeta med skydd
type: docs
weight: 90
url: /sv/java/working-with-protection/
---
## **Ställ in skydd för Visio Diagram**
 Skydda diagram tillåter användare att låsa bakgrunder, master (stenciler), former och stilar så att de inte kan redigeras. Detta är användbart för att skydda företagsstilar, till exempel, och säkerställa ett konsekvent utseende över en uppsättning diagram. Utvecklare kan uppnå detta med hjälp av[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).
### **Redigera skydd av Visio Diagram**
 Metoderna getProtectBkgnds, getProtectMasters, getProtectShapes och getProtectStyles, exponerade av[Dokumentinställningar](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentSettings) klass stöder com.aspose.diagram.BoolValue-objektet. Dessa egenskaper kan användas för att skydda och avskydda Microsoft Visio diagram.

I Microsoft Visio skyddar du dokument på detta sätt:

1. Öppna ett diagram i Microsoft Visio.
1. Öppna Ritningsutforskarens fönster.
1.  Högerklicka på en diagram och välj**Skydda dokument** från menyn.
1. I fönstret Skydda dokument markerar eller avmarkerar du alternativen för att låsa eller låsa upp olika diagram-element.
1.  Klick**OK**.

**Se hur vi kan kontrollera eller rensa alternativ manuellt.** 

![todo:image_alt_text](working-with-protection_1.png)

Använd koden nedan i en Java-applikation för att utföra samma uppgifter – låsa och låsa upp olika delar av din diagram – med Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Protection-VisioDiagramProtection-VisioDiagramProtection.java" >}}
### **Redigera Visio Shape Protection**
 Genom att skydda Visio-former kan användare låsa specifika aspekter av former. Aspekter av former som kan låsas genom formskydd inkluderar bredd, höjd, x-position, y-position, rotation med mera. Utvecklare kan uppnå detta med hjälp av[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

 De**getLockAspect()**, **getLockBegin()**, **getLockCalcWH()**, **getLockCrop()**, **getLockCustProp()**, **getLockDelete()**, **getLockEnd()**, **getLockFormat()**, **getLockFromGroupFormat()**, **getLockGroup()**, **getLockHeight()**, **getLockMoveX()**, **getLockMoveY()**, **getLockRotate()**, **getLockSelect()**, **getLockTextEdit()**, **getLockThemeColors()**, **getLockThemeEffects()**, **getLockVtxEdit()** och**getLockWidth()** metoder som exponeras av[Skydd](https://reference.aspose.com/diagram/java/com.aspose.diagram/Protection) klass stöder com.aspose.diagram.BoolValue-objektet. Dessa metoder kan användas för att skydda/avskydda former.

Visio måste du utföra följande åtgärder för att skydda alla former:

1. Öppna ett diagram i Microsoft Visio.
1. Välj en form.
1.  Välj**Skydd** från**Formatera** menyn (Visio 2007), eller välj**Skydd** från**Utvecklaren** meny (Visio 2010).
1.  I den**Skydd** fönster, välj eller rensa alternativ för att låsa eller låsa upp formattribut.
1.  Klick**OK**.

**En forms skyddsalternativ, som ses i Microsoft Visio** 

![todo:image_alt_text](working-with-protection_2.png)

Använd följande kod i din Java-applikation för att göra samma sak (låsa/låsa upp valfritt formattribut) med Aspose.Diagram for Java.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Protection-VisioShapeProtection-VisioShapeProtection.java" >}}
