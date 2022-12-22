---
title: Gruppera, konvertera och verifiera former
type: docs
weight: 50
url: /sv/java/group-convert-and-verify-shapes/
---
## **Gruppera flera former tillsammans i Visio-ritningen**
Aspose.Diagram API tillåter utvecklare att gruppera former för att flytta dem alla på en gång. Varje form i en grupp har en unik identitet och har sin egen uppsättning egenskaper. När vi ändrar formateringen av en grupp av former tilldelar den den nya egenskapen till varje form.
### **Hur man grupperar former**
Gruppmetoden som exponeras av klassen ShapeCollection kan användas för att gruppera former.

Koden nedan visar hur man:

1. Ladda ett prov diagram.
1. initierade en uppsättning av formerna
1. få en viss form genom id.
1. få en annan speciell form genom id.
1. tilldela former till arrayen.
1. gruppera former genom att anropa gruppmetoden.
1. spara diagram
#### **Programmeringsexempel för gruppformer**
Använd följande kod i din Java-applikation för att gruppera former med Aspose.Diagram for Java API.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-GroupShapes-GroupShapes.java" >}}
## **Konvertera en Visio Shape till andra filformat**
Aspose.Diagram for Java API tillåter utvecklare att konvertera en enda Visio-form till vilket annat filformat som helst. I den här artikeln tar vi bort alla andra Visio-former från sidan och anpassar sidinställningarna efter källans formstorlek.
### **Konvertera en viss Visio-form**
 Utvecklare kan konvertera en Visio-form till PDF, HTML, Image, SVG och SWF med[ange Visio sparalternativ]().
Den här exempelkoden fungerar enligt följande:

1. Ladda en källa Visio.
1. Skaffa en viss sida.
1. Ta bort bakgrundssidan.
1. Bygg en hashtabell med alla former som innehåller ID och namn.
1. Iterera genom hashtabellen
1. Ta bort alla former från Visio-sidan, utom den specifika.
1. Ställ in sidstorleken.
1. Spara sidan Visio i valfritt filformat som stöds.
#### **Konvertera formprogrammeringsexempel**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-SaveVisioShapeInOtherFormats-SaveVisioShapeInOtherFormats.java" >}}
### **Konvertera Visio Shape till PDF**
ToPdf-metoden för Shape-klassen gör det möjligt att konvertera en form till formatet PDF.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toPdf(dataDir + "out.pdf");

{{< /highlight >}}
### **Konvertera Visio Shape till HTML**
ToHTML-metoden för Shape-klassen gör det möjligt att konvertera en form till formatet HTML.

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

HTMLSaveOptions hs = new HTMLSaveOptions();

// save a shape in the PDF format

diagram.getPages().get(0).getShapes().getShape(59).toHTML(dataDir + "out.pdf", hs);

{{< /highlight >}}

{{% alert color="primary" %}} 

 Vi välkomnar dina frågor och förslag på[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Vi svarar omgående.

{{% /alert %}} 
## **Kontrollera om två Visio-former är anslutna eller limmade**
 Aspose.Diagram for Java API låter utvecklare verifiera att de två Visio-formerna är limmade eller sammankopplade. Tidigare har vi sett hur vi kan ansluta eller limma två former i dessa hjälpämnen:[Lägg till och anslut Visio Former](/diagram/sv/java/add-and-connect-visio-shapes/) och[Limma former inuti behållaren](/diagram/sv/java/working-with-shapes-gluing/).
### **Verifiering av de anslutna eller limmade formerna**
 De[Form](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class erbjuder egenskaperna IsGlued och IsConnected för att avgöra om två former är limmade eller sammankopplade.
#### **Verifiering av programmeringsprov för anslutna eller limmade former**
Följande kod verifierar om två former är sammankopplade eller limmade.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-VerifyConnectedOrGluedShapes-VerifyConnectedOrGluedShapes.java" >}}
## **Verifiera om Visio-formen är i en grupp av former**
Aspose.Diagram for Java API tillåter utvecklare att verifiera att Visio-formen är i en grupp av former eller inte.
### **Verifiering av form i gruppen av former**
Klassen Shape erbjuder IsInGroup-egenskaper för att avgöra om formen Visio är i en gruppform.
#### **Verifiering av form i gruppen av formprogrammeringsexempel**
Följande kodbit verifierar om formen är i en gruppform.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Shapes-VerifyShapeIsInGroup-VerifyShapeIsInGroup.java" >}}

{{% alert color="primary" %}} 

 Vi välkomnar dina frågor och förslag på[Aspose.Diagram Forum](https://forum.aspose.com/c/diagram/17). Vi svarar omgående.

{{% /alert %}}
