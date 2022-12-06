---
title: Ta bort formskyddet
type: docs
weight: 20
url: /sv/python-java/remove-shape-protection/
description: Det här avsnittet förklarar hur du tar bort formskyddet med Aspose.Diagram för Python via Java.
---
## **Ta bort skyddet för Visio-formen**
Genom att skydda Visio-former kan användare låsa specifika aspekter av former. Aspekter av former som kan låsas genom formskydd inkluderar bredd, höjd, x-position, y-position, rotation med mera. Utvecklare kan uppnå detta med Aspose.Diagram för Python via Java.
### **Redigera Visio Shape Protection**
**LockAspect**, **LockBegin**, **LockCalcWH**, **LockCrop**, **LockCustProp**, **LockDelete**, **LockEnd**, **LockFormat**, **LockFromGroupFormat**, **Låsgrupp**, **LockHeight**, **LockMoveX**, **LockMoveY**, **LåsRotera**, **LockSelect**, **LockTextEdit**, **LockThemeColors**, **LockThemeEffects**, **LockVtxEdit** och**LockWidth** fastigheter exponerade av**Skydd** klass stödja**Aspose.Diagram.BoolValue** objekt. Dessa egenskaper kan användas för att skydda och avskydda former.

I Microsoft Office Visio kan användaren utföra följande åtgärder för att skydda vilken form som helst:

- Öppet diagram i Microsoft Office Visio
- Välj valfri form
- Välj 'Skydd' från menyn 'Format' om du använder Visio 2007 eller välj 'Skydd' från menyn 'Utvecklare' om du använder Visio 2010
- I fönstret "Skydd", avmarkera en textruta för att låsa upp valfritt formattribut
- Tryck på 'Ok'

### **Ta bort formskyddsprogrammeringsprovet**
Använd följande kod i din applikation för att göra samma sak (låsa upp valfritt formattribut) med Aspose.Diagram för Python via Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-RemoveShapeProtection.py" >}}

