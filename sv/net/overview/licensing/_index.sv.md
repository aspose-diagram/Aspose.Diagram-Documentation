---
title: Licensiering
type: docs
weight: 50
url: /sv/net/licensing/
description: Aspose. Diagram for .NET bjuder in sina kunder att få en klassisk licens och mätlicens. Samt använda en begränsad licens för att bättre utforska produkten.
---
## **Värdera Aspose.Diagram**
Du kan enkelt ladda ner Aspose.Diagram for .NET produkt för utvärderingsändamål. Vänligen se[Aspose.Diagram for .NET nedladdningssida](https://www.nuget.org/packages/Aspose.Diagram/)för att ta reda på den senaste versionen. Nedladdningen av utvärderingen är densamma som den köpta nedladdningen. Utvärderingsversionen blir helt enkelt licensierad när du lägger till några rader kod för att tillämpa licensen.

Utvärderingsversionen av Aspose.Diagram (utan en angiven licens) ger full produktfunktionalitet, men den infogar en utvärderingsvattenstämpel i mitten av dokumentet vid öppna och spara, och begränsar till att endast läsa de tio första formerna på första sidan av din Visio diagram .

![todo:image_alt_text](licensing_1.png)
### **Begränsningar för utvärderingsversion**
Utvärderingsversionen innehåller alla funktioner utom följande:

- Du kan bara läsa de tio första formerna på första sidan av Visio diagram.
- Du kommer också att se utvärderingsvattenstämpel i exporterade bilder och PDF-filer.

{{% alert color="primary" %}} 

 Om du vill prova Aspose.Diagram utan utvärderingsbegränsningar, begär en 30 dagars tillfällig licens. Vänligen hänvisa till[Hur får man en tillfällig licens?](https://purchase.aspose.com/temporary-license) för mer information.

{{% /alert %}} 
## **Ansöker om en licens**
När du är nöjd med din[utvärdering](https://downloads.aspose.com/diagram/net) av Aspose.Diagram for .NET, köp en licens på webbplatsen Aspose:[Köpportal](https://purchase.aspose.com/buy) . Bekanta dig med de olika licenstyperna. Om du har några frågor,[kontakta Aspose säljteamet](https://about.aspose.com/contact) och de hjälper dig gärna.

Varje Aspose-licens innehåller en ettårsprenumeration för gratis uppgraderingar till alla nya versioner eller korrigeringar som kommer ut under denna tid. Vi tillhandahåller gratis och obegränsad teknisk support till både licensierade användare och utvärderingsanvändare.

Licensen är en XML-fil i vanlig text som innehåller detaljer som produktnamn, antal licensierade utvecklare, prenumerations utgångsdatum och så vidare. Filen är digitalt signerad, så ändra inte filen: även om du lägger till en extra radbrytning i filen blir den ogiltig.
### **När ska man ansöka om en licens**
Följ dessa enkla regler:

- Licensen behöver bara ställas in en gång per applikationsdomän.
- Du måste ställa in licensen innan du använder andra Aspose.Diagram-klasser.
- Att anropa SetLicense flera gånger är inte skadligt, men slösar bort processortid.
- Om du utvecklar en Windows Forms eller konsolapplikation, ring SetLicense i startkoden innan du använder Aspose.Diagram klasser.
- När du utvecklar en ASP.NET-applikation, anrop SetLicense från filen Global.asax.cs, i den skyddade metoden Aplication_Start. Den anropas en gång när applikationen startar.
- Anropa inte SetLicense från Page_Load-metoderna eftersom det betyder att licensen kommer att laddas varje gång en webbsida laddas.
- Om du utvecklar ett klassbibliotek anropar du SetLicense från en statisk konstruktor av klassen som använder Aspose.Diagram. Den statiska konstruktorn körs innan en instans av din klass skapas och ser till att Aspose.Diagram-licensen är korrekt inställd.
### **Tillämpa licens med File eller Stream Object**
 Använd[License.SetLicense](https://reference.aspose.com/diagram/net/aspose.diagram/license)metod för att licensiera komponenten. Det enklaste sättet att ställa in en licens är att lägga licensfilen i samma mapp som Aspose.Diagram.dll och ange filnamnet, utan sökväg, som visas nedan.
#### **Laddar en licens från fil**
Det här kodavsnittet initierar en licens som lagras i en fil eller i en inbäddad resurs.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// Set path of the license file, i.e. c:\temp\
string dataDir = @"c:\temp\";

License license = new License();
license.SetLicense(dataDir + "Aspose.Diagram.lic");

{{< /highlight >}}
```
#### **Ladda en licens från ett strömobjekt**
Dessa kodavsnitt initierar licensen från stream.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// Set path of the license file, i.e. c:\temp\
string dataDir = @"c:\temp\";
// Load an existing Visio file in the stream
FileStream LicStream = new FileStream(dataDir + "Aspose.Diagram.lic", FileMode.Open);

License license = new License();
license.SetLicense(LicStream);

{{< /highlight >}}
```
## **Tillämpa mätlicens**
Aspose.Diagram for .NET API tillåter utvecklare att tillämpa mätlicens. Det är en ny licensmekanism. Den nya licensmekanismen kommer att användas tillsammans med den befintliga licensmetoden. De kunder som vill bli fakturerade baserat på användningen av API-funktionerna kan använda den uppmätta licensen. För mer information, se[Metered Licensing FAQ](https://purchase.aspose.com/faqs/licensing/metered)sektion.

En ny klass[Uppmätt](https://reference.aspose.com/diagram/net/aspose.diagram/metered)har lagts till för att tillämpa mätt nyckel. Detta kodexempel visar hur man ställer in mätta offentliga och privata nycklar:

```
{{< highlight "csharp" >}}
// Initialize a Metered license class object
Aspose.Diagram.Metered metered = new Aspose.Diagram.Metered();
// apply public and private keys
metered.SetMeteredKey("your-public-key", "your-private-key");
{{< /highlight >}}
```
