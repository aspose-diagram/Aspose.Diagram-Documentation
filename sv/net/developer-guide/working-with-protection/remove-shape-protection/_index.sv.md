---
title: Ta bort formskyddet
type: docs
weight: 20
url: /sv/net/remove-shape-protection/
description: Det här avsnittet förklarar hur du tar bort formskyddet.
---
## **Ta bort skyddet för Visio-formen**
 Genom att skydda Visio-former kan användare låsa specifika aspekter av former. Aspekter av former som kan låsas genom formskydd inkluderar bredd, höjd, x-position, y-position, rotation med mera. Utvecklare kan uppnå detta med hjälp av[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Redigera Visio Shape Protection**
**LockAspect**, **LockBegin**, **LockCalcWH**, **LockCrop**, **LockCustProp**, **LockDelete**, **LockEnd**, **LockFormat**, **LockFromGroupFormat**, **Låsgrupp**, **LockHeight**, **LockMoveX**, **LockMoveY**, **LåsRotera**, **LockSelect**, **LockTextEdit**, **LockThemeColors**, **LockThemeEffects**, **LockVtxEdit** och**LockWidth** fastigheter exponerade av[**Skydd**](http://www.aspose.com/api/net/diagram/aspose.diagram/Protection) klass stödja**Aspose.Diagram.BoolValue** objekt. Dessa egenskaper kan användas för att skydda och avskydda former.

I Microsoft Office Visio kan användaren utföra följande åtgärder för att skydda vilken form som helst:

- Öppet diagram i Microsoft Office Visio
- Välj valfri form
- Välj 'Skydd' från menyn 'Format' om du använder Visio 2007 eller välj 'Skydd' från menyn 'Utvecklare' om du använder Visio 2010
- I fönstret "Skydd", avmarkera en textruta för att låsa upp valfritt formattribut
- Tryck på 'Ok'
### **Ta bort formskyddsprogrammeringsprovet**
Använd följande kod i din .NET-applikation för att göra samma sak (låsa upp valfritt formattribut) med Aspose.Diagram for .NET.

```
{{< highlight "csharp" >}}
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
```
