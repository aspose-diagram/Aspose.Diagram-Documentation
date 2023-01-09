---
title: Varför inte Automation
type: docs
weight: 70
url: /sv/java/why-not-automation/
---
{{% alert color="primary" %}} 

Varför är Aspose API:er ett mycket bättre alternativ än Microsoft Office Automation?

Det är två frågor som vi hör oftast här på Aspose:

1. **Kräver dina produkter Microsoft Office för att de ska kunna köras?** 
 Det enkla svaret är nej. Aspose API:er är helt oberoende och är inte anslutna till, inte heller auktoriserade, sponsrade eller på annat sätt godkända av Microsoft Corporation.
1. **Varför ska vi använda Aspose-produkter istället för att använda Microsoft Office-automatisering?** 
 Det kortaste svaret vi kan ge är att det finns många anledningar, där den främsta är att Microsoft själva starkt rekommenderar Office automatisering från mjukvarulösningar:[Överväganden för automatisering på serversidan av Office](https://support.microsoft.com/en-us/help/257757/considerations-for-server-side-automation-of-office).

Det finns flera anledningar till varför Aspose API:er är ett bättre alternativ till automatisering. Några av de viktigaste skälen är:

- [säkerhet](/diagram/sv/java/why-not-automation/)
- [Stabilitet](/diagram/sv/java/why-not-automation/)
- [Skalbarhet/hastighet](/diagram/sv/java/why-not-automation/)
- [Pris](/diagram/sv/java/why-not-automation/)
- [Funktioner](/diagram/sv/java/why-not-automation/)

De viktigaste punkterna beskrivs nedan. Se också till att besöka länkarna i slutet av det här avsnittet.

{{% /alert %}} 
### **säkerhet**
 Följande är ett direkt citat från den ovan refererade artikeln Microsoft:*"Office Applikationer var aldrig avsedda att användas på serversidan och tar därför inte hänsyn till säkerhetsproblemen som utsätts för distribuerade komponenter. Office autentiserar inte inkommande förfrågningar och skyddar dig inte från att oavsiktligt köra makron eller starta en annan server som kan köra makron från din kod på serversidan. Öppna inte filer som laddas upp till servern från en anonym webbsida! Baserat på de säkerhetsinställningar som senast ställdes in, kan servern köra makron under en administratörs- eller systemkontext med fullständig privilegier och äventyra ditt nätverk! Dessutom använder Office många komponenter på klientsidan (som Simple MAPI, WinInet och MSDAIPP) som kan cachelagra klientautentiseringsinformation för att påskynda bearbetningen. Om Office automatiseras på serversidan, en instans kan betjäna mer än en klient, och eftersom autentiseringsinformation har cachats för den sessionen är det möjligt att en klient kan använda cachen ed autentiseringsuppgifter för en annan klient, och därmed få icke-beviljade åtkomstbehörigheter genom att imitera andra användare."*

Aspose produkter är mycket säkra. Aspose API:er körs i samma användarkontext som alla .NET- och Java-applikationer. Därför utgör Aspose API:er inte en potentiell risk för viktiga systemresurser. Dessutom, när ett dokument öppnas av en Aspose API, körs makron inte automatiskt. Aspose API:er byggdes med målet att tillåta utvecklare att skapa, manipulera och spara Office filer. Ingen av riskerna förknippade med paketet Microsoft Office är inneboende i Aspose API:er.
### **Stabilitet**
 Följande är ett direkt citat från den ovan refererade artikeln Microsoft:*"Office 2000, Office XP och Office 2003 använd Microsoft Windows Installer-teknik (MSI) för att göra installation och självreparation enklare för en slutanvändare. MSI introducerar konceptet "installeras på första gången" eller konfigureras vid körning (för systemet, eller oftare för en viss användare). I en miljö på serversidan saktar detta både ned prestanda och ökar sannolikheten för att en dialogruta kan visas som ber användaren att godkänna installationen eller tillhandahålla en lämplig installationsskiva. Även om den är utformad för att öka motståndskraften hos Office som en slutanvändarprodukt, är Office:s implementering av MSI-funktioner kontraproduktiv i en miljö på serversidan. Dessutom kan stabiliteten hos Office i allmänhet inte garanteras när servern körs -sidan eftersom den inte har designats eller testats för denna typ av användning. Att använda Office som en tjänstkomponent på en nätverksserver kan minska stabiliteten för den maskinen och som en följd av ditt nätverk som helhet. Om du planerar att automatisera Office serversidan, försök att isolera programmet till en dedikerad dator som inte kan påverka kritiska funktioner och som kan startas om vid behov."*

Eftersom Aspose API:er är paketerade i ett enda bibliotek, kommer det aldrig att finnas ett behov av att installera några ytterligare delar eller delar för att de ska fungera. Aspose API:er används av olika applikationer och det finns ingen del av API-koden utformad för att vänta på ett mänskligt svar. Aspose API:er har testats noggrant. Aspose API:er används av företag som IBM , Hilton , Reader's Digest, Bank of America och många fler.
### **Skalbarhet/hastighet**
 Följande är ett direkt citat från den ovan refererade artikeln Microsoft:*"Serversidans komponenter måste vara mycket återkommande, flertrådiga COM-komponenter med minimal overhead och hög genomströmning för flera klienter. Office Applikationer är i nästan alla avseenden raka motsatsen. De är icke-återkommande, STA-baserade automationsservrar som är designade för att tillhandahålla mångsidig men resurskrävande funktionalitet för en enskild klient. De erbjuder liten skalbarhet som en lösning på serversidan och har fasta gränser för viktiga element, som minne, som inte kan ändras genom konfiguration. Ännu viktigare, de använder globala resurser (som minneskartade filer, globala tillägg eller mallar och delade automationsservrar), som kan begränsa antalet instanser som kan köras samtidigt och leda till tävlingsförhållanden om de är konfigurerade i en multiklientmiljö. planerar att köra mer än en instans av en Office-applikation samtidigt måste överväga att "poola" eller serialisera åtkomst till Office-applikationen för att undvika pote ursprungliga låsningar eller datakorruption."*

Aspose API:er är mycket skalbara och blixtsnabba. Office-applikationer var inte designade för att användas samtidigt av hundratals och tusentals användare; dock är Aspose API:er designade för just det. Våra API:er är en sann lösning och fungerar felfritt oavsett om det är på en enda server som driver en enda applikation eller på en belastningsbalanserad webbfarm som driver en företagsomfattande applikation.
### **Pris**
 När en applikation använder Microsoft Office automation måste en kopia av Microsoft Office köpas för varje maskin som kör applikationen. Det finns många gånger som ett program kan behöva skapa eller manipulera en office-fil, men kräver inte att användaren har Office. Aspose erbjuder en mycket[kostnadseffektiv](https://purchase.aspose.com/), royaltyfri, omfördelningslicens som kommer att tillåta distribution till ett obegränsat antal användare utan licensbekymmer.

När du skapar webbaserade applikationer är det viktigt att veta att Microsoft Office automationskomponenter inte är prissatta eller licensierade för serversidans lösningar; därför finns det ingen bra licenslösning för att distribuera webbapplikationer som använder Microsoft Office-komponenterna. Aspose erbjuder en mycket kostnadseffektiv lösning även för serverbaserade applikationer.
### **Funktioner**
 Aspose-komponenter tillhandahåller allt som behövs för att hantera Office-filer, plus mycket, mycket mer. De är designade med filosofin att tillåta utvecklare att uppnå de bästa resultaten med minsta möjliga arbete. Till skillnad från Office automation ger Aspose komponenter många kraftfulla, tidsbesparande funktioner. Till exempel,[Aspose.Diagram](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram) erbjuder utvecklare möjligheten att exportera från en**Datatabell** eller**DataView** direkt till en Excel-fil.[Varje komponent](https://products.aspose.com/total) i Aspose-familjen erbjuder sina egna unika, kraftfulla funktioner.

Det bästa med att köpa en Aspose API eller en API-svit är att ha tillgång till våra utvecklingsteam. Våra utvecklingsteam inser att om det finns en funktion som ditt företag behöver, är det mer än troligt att andra företag kommer att behöva det också. Även om inte alla funktionsförfrågningar kan läggas till, försöker våra team att vara väldigt öppna och flexibla när de tillhandahåller hjälp. Det tänkesättet är det som har hjälpt Aspose API:er att bli lika kraftfulla som de är. Om det finns ytterligare funktioner som du behöver från Office automationsobjekt, är dina chanser att lägga till dem mycket, mycket låga.
### **Slutsats**
{{% alert color="primary" %}} 

 Den här artikeln har tagit upp nyckelpunkterna om varför Aspose API:er är ett bättre val än Office automatisering. Alla de olika Aspose API:erna erbjuder en riskfri, utan förpliktelse[utvärderingsversion](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram). Vi uppmuntrar dig att dra nytta av den utvärderingen för att se vad Aspose kan göra för dina ansökningar.

För mer information, vänligen navigera till denna internetartikel:

- [Överväganden för Server-Side Automation av Office](https://support.microsoft.com/en-us/help/257757/considerations-for-server-side-automation-of-office)

{{% /alert %}}
