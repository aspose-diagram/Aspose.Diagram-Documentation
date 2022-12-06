---
title: Använder Aspose.Diagram i andra programmeringsspråk
type: docs
weight: 120
url: /sv/net/utilizing-aspose-diagram-in-other-programming-languages/
description: Den här sidan beskriver hur du använder Aspose.Diagram i andra programmeringsspråk.
---
## **Använd Aspose.Diagram for .NET via COM Interop**
 Informationen i det här ämnet gäller scenarier där utvecklare behöver använda[Aspose.Diagram for .NET](/diagram/sv/net/home/) via COM Interop på alla språk som stöds.
### **Arbetar med COM Interop**
Aspose.Diagram for .NET körs under kontroll av .NET Framework och detta kallas hanterad kod. Koden som är skriven på alla språk som körs utanför .NET Framework och den kallas ohanterad kod. Interaktion mellan ohanterad kod och Aspose.Diagram sker via funktionen .NET som kallas COM Interop.

Aspose.Diagram-objekt är .NET-objekt, men när de används via COM Interop visas de som COM-objekt i ditt programmeringsspråk. Därför är det bäst att se till att du vet hur du skapar och använder COM-objekt i ditt programmeringsspråk innan du börjar använda[Aspose.Diagram for .NET](/diagram/sv/net/home/).

- I COM-världen skiljer vi COM-server och COM-klient. COM-servern lagrade COM-klasser medan COM-klienten frågar COM-servern om klassinstanser, dvs COM-objekt.
-  COM-klient eller helt enkelt klientapplikation kan känna till något om COM-klassinnehåll eller vara helt omedveten om dess metoder och egenskaper. Därför kan klientapplikationen upptäcka COM-klassstrukturen vid kompilering/byggande eller endast under körning. Processen för "upptäckt" är känd som bindande och så har vi**tidig bindning** och**sen bindning**.
-  korthet COM-klass är som en svart låda och för att arbeta med den behövs typbibliotek, denna binära fil har beskrivningar av COM-klassmetoder, egenskaper och alla språk på hög nivå som stöder arbete med COM-objekt har ofta syntaxuttryck för att lägga till typbibliotek, för exempel detta är[**#importera**](http://msdn.microsoft.com/en-us/library/8etzzkb6.aspx) på C++.
- typbibliotek används för tidig bindning.
-  ett COM-objekt kan exponera sina metoder och egenskaper på två sätt: med hjälp av en**utskickningsgränssnitt** (dispinterface) och i dess**vtabell** (virtuell funktionstabell).
-  inom**dispinterface** , varje metod och egenskap identifieras av en unik medlem; denna medlem är funktionens avsändningsidentifierare (eller**DispID**).
- **vtabell** är bara en uppsättning pekare till funktioner som COM-klassgränssnittet stöder.
-  ett objekt som exponerar sina metoder genom båda gränssnitten stöder en**dubbla gränssnitt**.
- det finns fördelar med båda typerna av bindning. Tidig bindning ger dig ökad prestanda och syntaxkontroll vid kompilering. Sen bindning är mest fördelaktigt när du skriver kunder som du tänker bli***kompatibel med framtida versioner*** av din COM-klass. Med sen bindning är information från typbiblioteket inte "hårdkopplad" till din klient, så du kan ha större förtroende för att din klient kan arbeta med framtida versioner av COM-klass utan kodändringar.
-  sen bindningsmekanism har en stor fördel: om skaparen av COM DLL bestämmer sig för att släppa en ny version, med en annan funktionsgränssnittslayout, kommer kod som anropar dessa metoder inte att krascha om inte metoderna inte längre är tillgängliga; även om**vtabell**är annorlunda sen bindning lyckas upptäcka de nya DISPID:erna och anropa lämpliga metoder.

 Här är de ämnen som du så småningom kommer att behöva bemästra:

- Använda COM-objekt i ditt programmeringsspråk. Se dokumentationen för ditt programmeringsspråk och de språkspecifika ämnena längre fram i denna dokumentation.
-  Arbeta med COM-objekt exponerade av .NET COM Interop. Ser[Samverkan med ohanterad kod](https://docs.microsoft.com/en-us/dotnet/framework/interop/) och[Exponera .NET Framework komponenter för COM](https://docs.microsoft.com/en-us/dotnet/framework/interop/exposing-dotnet-components-to-com) i MSDN.
-  Aspose.Diagram dokumentobjektmodell. Ser[Aspose.Diagram Programmeringsguide](https://docs.aspose.com/diagram/net/developer-guide/) och[API Referens](https://reference.aspose.com/diagram/net).
#### **Registrera Aspose.Diagram for .NET med COM Interop**
Du måste installera Aspose.Diagram for .NET och se till att den är registrerad hos COM Interop (försäkra dig om att den kan anropas från ohanterad kod).

För att registrera Aspose.Diagram for .NET för COM Interop manuellt:

1.  Från**Start** menyn, välj**Alla program** , då**Microsoft Visual Studio**, **Visual Studio-verktyg** och slutligen,**Visual Studio Kommandotolk**. I vissa operativsystem är det också tillgängligt på platsen: "C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\bin\x64"
1.  Ange kommandot för att registrera församlingen:
   1. .NET Framework 2.0
regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net2.0\Aspose.Diagram.dll" /codebase
   1. .NET Framework 3.5
 regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net3.5\Aspose.Diagram.dll" /codebase
   1. .NET Framework 4.0
 regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net4.0\Aspose.Diagram.dll" /codebase

{{% alert color="primary" %}} 

Var uppmärksam på att /codebase endast är nödvändig om Aspose.Diagram.dll inte finns i GAC, om du använder det här alternativet görs regasm-sökvägen för montering i registret.

{{% /alert %}} {{% alert color="primary" %}} 

 regasm.exe är ett verktyg som ingår i .NET Framework SDK. Alla .NET Framework SDK-verktyg finns i*\Microsoft .NET\Framevork\<FrameworkVersion>* katalog, till exempel*C:\Windows\Microsoft .NET\Framework\v4.0.30319*. Om du använder Visual Studio .NET:
 Från**Start** menyn, välj**Program** , följd av**Microsoft Visual Studio .NET** , då**Visual Studio .NET Verktyg** och slutligen,**Visual Studio .NET 2003 Kommandotolk**.
Den kör en kommandotolk med alla nödvändiga miljövariabler inställda.

{{% /alert %}} 
##### **ProgIDs**
ProgID står för "programmatic identifier". Det är namnet på en COM-klass som används för att skapa ett objekt. ProgID består av biblioteksnamnet "Aspose.Diagram" och klassnamnet.
##### **Skriv bibliotek**
Om ditt programmeringsspråk (till exempel Visual Basic eller Delphi) tillåter dig att referera till ett bibliotek av COM-typ, lägg sedan till en referens till Aspose.Diagram.tlb och för att se alla Aspose.Diagram for .NET klasser, metoder, egenskaper och uppräkningar i din objektläsare.

Så här genererar du en TLB-fil:

- .NET Framework 2.0
 regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net2.0\Aspose.Diagram.dll" /tlb: "C:\Program Files\Aspose\Aspose.Diagram\Aspose.Diagram/Aspose.Diagram Aspose.Diagram Aspose.Diagram 4276t\076t.net\076t.
- .NET Framework 3.5
 regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net3.5\Aspose.Diagram.dll" /tlb: "C:\Program Files\Aspose\Aspose.Diagram\Aspose.Diagram/Aspose.Diagram Aspose.Diagram Aspose.Diagram Aspose.Diagram 4376t.net\076t.
- .NET Framework 4.0
regasm "C:\Program Files\Aspose\Aspose.Diagram for .NET\bin\net4.0\Aspose.Diagram.dll" /tlb: "C:\Program Files\Aspose\Aspose.Diagram\Aspose.Diagram/Aspose.Diagram Aspose.Diagram Aspose.Diagram 476t.net\076t.net\476t.
#### **Skapa COM-objekt**
Skapandet av ett COM-objekt liknar skapandet av ett vanligt .NET-objekt. När du väl har skapat det kan du komma åt objektets metoder och egenskaper, som om det vore ett COM-objekt.

Vissa metoder har överbelastning och de kommer att exponeras av COM Interop med ett numeriskt suffix lagt till dem, förutom den allra första metoden som förblir oförändrad. Till exempel blir Diagram.Save-metodens överbelastningar Diagram.Save, Diagram.Save_2, och så vidare.

{{% alert color="primary" %}} 

 För mer information, se de språkspecifika artiklarna längre fram i denna dokumentation.

{{% /alert %}} 
## **Aspose.Diagram Resurser**
Följande är länkarna till några användbara resurser som du kan behöva för att utföra dina uppgifter.
- [Aspose.Diagram for Java Onlinedokumentation](https://docs.aspose.com/diagram/java/)
- [Aspose.Diagram för Node.js via Java onlinedokumentation](https://docs.aspose.com/diagram/nodejsjava/)
- [Aspose.Diagram för Python via Java Onlinedokumentation](https://docs.aspose.com/diagram/pythonjava/)

##### **Skapa en omslagsenhet**
Om du behöver använda många av Aspose.Diagram for .NET klasser, metoder och egenskaper, överväg att skapa en omslagssammansättning (med C# eller något annat .NET programmeringsspråk). Omslagsenheter hjälper till att undvika att använda Aspose.Diagram for .NET direkt från ohanterad kod.

Ett bra tillvägagångssätt är att utveckla en .NET-sammansättning som refererar till Aspose.Diagram for .NET och gör allt arbete med det, och bara exponerar en minimal uppsättning klasser och metoder för ohanterad kod. Din applikation bör då bara fungera med ditt omslagsbibliotek.

 Att minska antalet klasser och metoder som du behöver anropa via COM Interop förenklar projektet. Att använda .NET klasser via COM Interop kräver ofta avancerade färdigheter.
## **Skapa en tom Visio-ritning i PHP med COM Interop**
### **Förutsättningar**
 Konfigurera din PHP för att fungera med COM. Ser<http://www.php.net/manual/en/ref.com.php> . För mer information, vänligen kontrollera artikeln med namnet[Använd Aspose.Diagram for .NET via COM Interop](/diagram/sv/net/home/).
### **Skapa en tom Visio Ritning**
 Detta är en enkel applikation som visar hur du skapar en tom Visio ritning med hjälp av[Aspose.Diagram for .NET](/diagram/sv/net/home/) i PHP via COM Interop.

**PHP**

{{< highlight "csharp" >}}

 <?php

echo "<h3>Calling Aspose.Diagram for .NET from PHP using COM Interoperatibility</h3>";

//set license

$lic = new COM("Aspose.Diagram.License");

$lic->SetLicense("D:\ASPOSE\Licences\Aspose.Total licenses\Aspose.Total.lic");

// create a new instance of Diagram object using COM interop

$diagram = new COM("Aspose.Diagram.Diagram");

// Save the Visio drawing in the VDX format

$diagram->Save("d:\diagramtest\MyOutput.vdx", 0);

?>



{{< /highlight >}}
