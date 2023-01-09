---
title: Beräkna stiftvärden och inställningsstorlek för en form
type: docs
weight: 40
url: /sv/java/calculate-pin-values-and-setting-size-of-a-shape/
---
## **Beräkna PinX- och PinY-värden för underformen**
 Om formen är en underordnad gruppform är dens xform en relativ koordinat av dess överordnade form, men inte absolut koordinat i[Sida](https://reference.aspose.com/diagram/java/com.aspose.diagram/page). Om användaren behöver få den absoluta koordinaten hjälper den här exempelkoden.

En punkt specificerad i lokala koordinater kan omvandlas till överordnade koordinater genom att tillämpa följande transformationer i följande ordning:

1. Subtrahera värdet för egenskapen LocPinX för elementet Cell_Type från x-koordinaten.
1. Subtrahera värdet för egenskapen LocPinY för Cell_Type från y-koordinaten.
1. Spegla punkten kring y-axeln om värdet på egenskapen FlipX för Cell_Type är lika med ett.
1. Spegla punkten kring x-axeln om värdet på egenskapen FlipY för Cell_Type är lika med ett.
1. Rotera punkten moturs runt origo med värdet på egenskapen Angle för Cell_Type.
1. Lägg till värdet för PinX Cell_Type till x-koordinaten.
1. Lägg till värdet för PinY Cell_Type till y-koordinaten.
### **Beräkna PinX och PinY programmeringsexempel**
Använd följande kod i din Java-applikation för att beräkna PinX- och PinY-värden för en underform med Aspose.Diagram for Java API.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-CalculateCenterOfSubShapes-CalculateCenterOfSubShapes.java" >}}
## **Ställa in höjd och bredd på en form**
 De[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) Klass låter dig styra formstorleken genom att ange höjd och bredd på formen med metoderna SetHeight och SetWidth.

 Metoderna SetHeight och SetWidth, exponerade av[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape)klass, stöder storleksändring av en form med mastern, utan mastern eller i form av en gruppform.

Kodexemplen i den här artikeln ställer in höjd och bredd för att ändra storlek på formen på sidan.

**Ingång diagram** 

![todo:image_alt_text](http://i.imgur.com/cTiNWa7.png)

**diagram efter att höjd och bredd har ändrats**

![todo:image_alt_text](calculate-pin-values-and-setting-size-of-a-shape_1.png)

Processen för att ställa in höjd och bredd är:

1. Ladda ett diagram.
1. Hitta en viss form.
1. Ställ in höjden på en form.
1. Ställ in bredden på en form.
1. Spara diagram.
### **Inställning av höjd och bredd Programmeringsexempel**
Kodavsnittet nedan visar hur du ställer in formens höjd och bredd. Koden letar efter en formnamnsrektangel, med form-ID 1, och ställer in dess höjd och bredd som dubbla.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-ChangeShapeSize-ChangeShapeSize.java" >}}
