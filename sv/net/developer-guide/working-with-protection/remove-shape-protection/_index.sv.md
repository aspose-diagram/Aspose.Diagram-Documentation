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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Protection-RemoveShapeProtection-RemoveShapeProtection.cs" >}}
