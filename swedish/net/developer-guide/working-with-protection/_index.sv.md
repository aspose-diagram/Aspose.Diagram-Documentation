---
title: Arbeta med skydd
type: docs
weight: 170
url: /sv/net/working-with-protection/
description: Det här avsnittet förklarar hur du ställer in skydd i diagram med Aspose.Diagram.
---
## **Ställ in skydd för Visio Diagram**
 Skydda diagram tillåter användare att låsa bakgrunder, master (stenciler), former och stilar så att de inte kan redigeras. Detta är användbart för att skydda företagsstilar, till exempel, och säkerställa ett konsekvent utseende över en uppsättning diagram. Utvecklare kan uppnå detta med hjälp av[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Redigera Visio Diagram Skydd**
Egenskaperna ProtectBkgnds, ProtectMasters, ProtectShapes och ProtectStyles, exponerade av[Dokumentinställningar](http://www.aspose.com/api/net/diagram/aspose.diagram/documentsettings) klass stöder objektet Aspose.Diagram.BoolValue. Dessa egenskaper kan användas för att skydda och avskydda Microsoft Office Visio diagram. I Microsoft Visio skyddar du dokument på detta sätt:

1. Öppna ett diagram i Microsoft Visio.
1. Öppna Ritningsutforskarens fönster.
1.  Högerklicka på en diagram och välj**Skydda dokument** från menyn.
1. I fönstret Skydda dokument markerar eller avmarkerar du alternativen för att låsa eller låsa upp olika diagram-element.
1.  Klick**OK**.
#### **Redigera Diagram skyddsprogrammeringsexempel**
Använd koden nedan i en .NET-applikation för att utföra samma uppgifter som att låsa och låsa upp olika delar av Visio diagram med Aspose.Diagram for .NET API.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Protection-VisioDiagramProtection-VisioDiagramProtection.cs" >}}
## **Ställ in skydd av formen Visio**
 Genom att skydda Visio-former kan användare låsa specifika aspekter av former. Aspekter av former som kan låsas genom formskydd inkluderar bredd, höjd, x-position, y-position, rotation med mera. Utvecklare kan uppnå detta med hjälp av[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Redigera Visio Shape Protection**
**LockAspect**, **LockBegin**, **LockCalcWH**, **LockCrop**, **LockCustProp**, **LockDelete**, **LockEnd**, **LockFormat**, **LockFromGroupFormat**, **Låsgrupp**, **LockHeight**, **LockMoveX**, **LockMoveY**, **LåsRotera**, **LockSelect**, **LockTextEdit**, **LockThemeColors**, **LockThemeEffects**, **LockVtxEdit** och**LockWidth** fastigheter exponerade av[**Skydd**](http://www.aspose.com/api/net/diagram/aspose.diagram/Protection) klass stödja**Aspose.Diagram.BoolValue** objekt. Dessa egenskaper kan användas för att skydda och avskydda former.

I Microsoft Office Visio kan användaren utföra följande åtgärder för att skydda vilken form som helst:

- Öppet diagram i Microsoft Office Visio
- Välj valfri form
- Välj 'Skydd...' från menyn 'Format' om du använder Visio 2007 eller välj 'Skydd' från menyn 'Utvecklare' om du använder Visio 2010
- I fönstret 'Skydd', markera/avmarkera en textruta för att låsa eller låsa upp ett formattribut
- Tryck på 'Ok'
### **Redigera formskyddsprogrammeringsexemplet**
Använd följande kod i din .NET-applikation för att göra samma sak (låsa/låsa upp valfritt formattribut) med Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Protection-VisioShapeProtection-VisioShapeProtection.cs" >}}
