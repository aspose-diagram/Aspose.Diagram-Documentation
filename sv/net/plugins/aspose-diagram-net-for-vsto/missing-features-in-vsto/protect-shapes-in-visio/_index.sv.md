---
title: Skydda former i Visio
type: docs
weight: 20
url: /sv/net/protect-shapes-in-visio/
---
LockAspect, LockBegin, LockCalcWH, LockCrop, LockCustProp, LockDelete, LockEnd, LockFormat, LockFromGroupFormat, LockGroup, LockHeight, LockMoveX, LockMoveY, LockRotate, LockSelect, LockTextEdit, LockThemeColors, LockThemeEffects, LockVtxEdit and LockWidth properties exposed by Protection class support the Aspose.Diagram.BoolValue object . Dessa egenskaper kan användas för att skydda/avskydda former.

Visio måste du utföra följande åtgärder för att skydda alla former:

- Öppna diagram i MS Visio
- Välj valfri form
- Välj 'Skydd...' från menyn 'Format' om du använder Visio 2007 eller välj 'Skydd' från menyn 'Utvecklare' om du använder Visio 2010
- I fönstret 'Skydd', markera/avmarkera en textruta för att låsa eller låsa upp ett formattribut
- Tryck på 'Ok'

Använd följande kod i din .NET-applikation för att göra samma sak (låsa valfritt formattribut) med Aspose.Diagram for .NET.

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
## **Ladda ner exempelkod**
- [Bit hink](https://bitbucket.org/asposemarketplace/aspose-for-vsto/src/master/Aspose.Diagram%20Vs%20VSTO%20Visio/)
