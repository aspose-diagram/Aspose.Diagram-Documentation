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

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VisioDiagramProtection.class);
//Load diagram
Diagram diagram = new Diagram(dataDir + "ProtectAndUnprotect.vsd");

diagram.getDocumentSettings().setProtectBkgnds(BOOL.TRUE);
diagram.getDocumentSettings().setProtectMasters(BOOL.TRUE);
diagram.getDocumentSettings().setProtectShapes(BOOL.TRUE);
diagram.getDocumentSettings().setProtectStyles(BOOL.TRUE);
// save diagram
diagram.save(dataDir + "VisioDiagramProtection_Out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
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
shape.getProtection().getLockAspect().setValue(BOOL.TRUE);
shape.getProtection().getLockBegin().setValue(BOOL.TRUE);
shape.getProtection().getLockCalcWH().setValue(BOOL.TRUE);
shape.getProtection().getLockCrop().setValue(BOOL.TRUE);
shape.getProtection().getLockCustProp().setValue(BOOL.TRUE);
shape.getProtection().getLockDelete().setValue(BOOL.TRUE);
shape.getProtection().getLockEnd().setValue(BOOL.TRUE);
shape.getProtection().getLockFormat().setValue(BOOL.TRUE);
shape.getProtection().getLockFromGroupFormat().setValue(BOOL.TRUE);
shape.getProtection().getLockGroup().setValue(BOOL.TRUE);
shape.getProtection().getLockHeight().setValue(BOOL.TRUE);
shape.getProtection().getLockMoveX().setValue(BOOL.TRUE);
shape.getProtection().getLockMoveY().setValue(BOOL.TRUE);
shape.getProtection().getLockRotate().setValue(BOOL.TRUE);
shape.getProtection().getLockSelect().setValue(BOOL.TRUE);
shape.getProtection().getLockTextEdit().setValue(BOOL.TRUE);
shape.getProtection().getLockThemeColors().setValue(BOOL.TRUE);
shape.getProtection().getLockThemeEffects().setValue(BOOL.TRUE);
shape.getProtection().getLockVtxEdit().setValue(BOOL.TRUE);
shape.getProtection().getLockWidth().setValue(BOOL.TRUE);
        
// save diagram
diagram.save(dataDir + "VisioShapeProtection_Out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
