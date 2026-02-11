---
title: Licensiering
type: docs
weight: 60
url: /sv/java/licensing/
---
## **Begränsningar för utvärderingsversion**
 En gratis utvärderingsversion av Aspose.Diagram for Java kan laddas ner från[Aspose Förvar](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram).
### **Begränsning**
Utvärderingsversionen innehåller alla funktioner utom följande:

- Du kan bara läsa de tio första formerna på första sidan i din VSD-fil.
- Du kommer också att se utvärderingsvattenstämpel i exoprerade bilder och PDF-filer.

 Om du vill prova Aspose.Diagram utan utvärderingsbegränsningar, begär en 30 dagars tillfällig licens. Vänligen hänvisa till[Hur får man en tillfällig licens?](https://purchase.aspose.com/temporary-license) för mer information.
## **Ansöker om en licens**
 Du kan ladda ner en utvärderingsversion av**Aspose.Diagram** for Java från[Aspose Förvar](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram). Utvärderingsversionen ger absolut samma möjligheter som den licensierade versionen av produkten. Dessutom blir utvärderingsversionen helt enkelt licensierad när du köper en licens och lägger till ett par rader kod för att tillämpa licensen.

 När du är nöjd med din utvärdering av**Aspose.Diagram** , du kan[köpa en licens](https://purchase.aspose.com/buy) på webbplatsen Aspose. Bekanta dig med de olika prenumerationstyperna som erbjuds. Om du har några frågor, tveka inte att kontakta Aspose säljteamet.

Varje Aspose-licens innehåller en ettårsprenumeration för gratis uppgraderingar till alla nya versioner eller korrigeringar som kommer ut under denna tid. Teknisk support är gratis och obegränsad och tillhandahålls både till licensierade användare och utvärderingsanvändare.

{{% alert color="primary" %}} 

 Om du vill testa**Aspose.Diagram** utan begränsningar i utvärderingsversionen, begär en 30-dagars tillfällig licens. Vänligen hänvisa till[Hur får man en tillfällig licens?](https://purchase.aspose.com/temporary-license) för mer information.

{{% /alert %}} 
### **Ställa in en licens**
Licensen är en XML-fil i vanlig text som innehåller detaljer som produktnamn, antal utvecklare den är licensierad till, prenumerationsutgångsdatum och så vidare. Filen är digitalt signerad, så ändra inte filen; även ett oavsiktligt tillägg av en extra radbrytning i filen kommer att ogiltigförklara den.

Du måste ansöka om en licens innan du utför några operationer med dokument. Se till att du gör detta innan du skapar ett Diagram-objekt. Du behöver bara ange en licens en gång per ansökan eller process.

Licensen kan laddas från en stream eller fil på följande platser:

1. Explicit väg.
1. Mappen som innehåller Aspose.Diagram.jar.

 Använd[License.setLicense()](https://reference.aspose.com/diagram/java/com.aspose.diagram/License) metod för att licensiera komponenten. Ofta är det enklaste sättet att ställa in en licens att lägga licensfilen i samma mapp som Aspose.Diagram.jar och ange bara filnamnet utan sökväg som visas i följande exempel:
#### **Exempel 1**
 I detta exempel**Aspose.Diagram** kommer att försöka hitta licensfilen i mappen som innehåller JAR:erna för din applikation.

**Java**

{{< highlight "csharp" >}}

 com.aspose.diagram.License license = new com.aspose.diagram.License();

license.setLicense("Aspose.Diagram.Java.lic");

{{< /highlight >}}
#### **Exempel 2**
Initierar en licens från en stream.

**Java**

{{< highlight "csharp" >}}

 com.aspose.diagram.License license = new com.aspose.diagram.License();

license.setLicense(new java.io.FileInputStream("Aspose.Diagram.Java.lic"));

{{< /highlight >}}
### **Validera licensen**
 Det är möjligt att validera om licensen är korrekt inställd eller inte. De[Licens](https://reference.aspose.com/diagram/java/com.aspose.diagram/License)klass har fältet isLicensed som returnerar sant om licensen har ställts in korrekt.

**Java**

{{< highlight "csharp" >}}

 License license = new License();

license.setLicense("Aspose.Diagram.Java.lic");

if (License.isLicensed()) {

    System.out.println("License is Set!");

}

{{< /highlight >}}
## **Tillämpa mätlicens**
Aspose.Diagram for Java API tillåter utvecklare att tillämpa mätlicens. Det är en ny licensmekanism. Den nya licensmekanismen kommer att användas tillsammans med den befintliga licensmetoden. De kunder som vill bli fakturerade baserat på användningen av API-funktionerna kan använda den uppmätta licensen. För mer information, se[Metered Licensing FAQ](https://purchase.aspose.com/faqs/licensing/metered)sektion.

En ny klass[Uppmätt](https://reference.aspose.com/diagram/java/com.aspose.diagram/Metered) har lagts till för att tillämpa mätt nyckel. Detta kodexempel visar hur man ställer in mätta offentliga och privata nycklar:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// Initialize a Metered license class object
Metered metered = new Metered();
// apply public and private keys
metered.setMeteredKey("your-public-key", "your-private-key");
{{< /highlight >}}
```
