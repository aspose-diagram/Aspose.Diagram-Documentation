---
title: Beräkna stiftvärden och inställningsstorlek för en form
type: docs
weight: 60
url: /sv/net/calculate-pin-values-and-setting-size-of-a-shape/
description: Det här avsnittet förklarar hur man beräknar PinX- och PinY-värden för underformen med Aspose.Diagram.
---
## **Beräkna PinX- och PinY-värden för underformen**
 Om formen är en undernod med gruppform, är dess xform en relativ koordinat av dess överordnade form men inte absolut koordinat i[Sida](http://www.aspose.com/api/net/diagram/aspose.diagram/page). Om användaren behöver få den absoluta koordinaten hjälper den här exempelkoden.

En punkt specificerad i lokala koordinater kan omvandlas till överordnade koordinater genom att tillämpa följande transformationer i följande ordning:

1. Subtrahera värdet för egenskapen LocPinX för elementet Cell_Type från x-koordinaten.
1. Subtrahera värdet för egenskapen LocPinY för Cell_Type från y-koordinaten.
1. Spegla punkten kring y-axeln om värdet på egenskapen FlipX för Cell_Type är lika med ett.
1. Spegla punkten kring x-axeln om värdet på egenskapen FlipY för Cell_Type är lika med ett.
1. Rotera punkten moturs runt origo med värdet på egenskapen Angle för Cell_Type.
1. Lägg till värdet för PinX Cell_Type till x-koordinaten.
1. Lägg till värdet för PinY Cell_Type till y-koordinaten.
### **Beräkna PinX och PinY programmeringsexempel**
Använd följande kod i din .NET-applikation för att beräkna PinX- och PinY-värden för en underform med Aspose.Diagram for .NET API.







{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-CalculateCenterOfSubShapes-CalculateCenterOfSubShapes.cs" >}}
## **Ställa in höjd och bredd på en form**
 De[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) Klass låter dig styra formstorleken genom att ange höjd och bredd på formen med metoderna SetHeight och SetWidth.

 Metoderna SetHeight och SetWidth, exponerade av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape)klass, stöder storleksändring av en form med mastern, utan mastern eller i form av en gruppform. Kodexemplen i den här artikeln ställer in höjd och bredd för att ändra storlek på formen på sidan.

Processen för att ställa in höjd och bredd är:

1. Ladda ett diagram.
1. Hitta en viss form.
1. Ställ in höjden på en form.
1. Ställ in bredden på en form.
1. Spara diagram.
### **Inställning av höjd och bredd Programmeringsexempel**
Kodavsnittet nedan visar hur du ställer in formens höjd och bredd. Koden letar efter en formnamnsrektangel, med form-ID 1, och ställer in dess höjd och bredd som dubbla.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-ChangeShapeSize-ChangeShapeSize.cs" >}}
