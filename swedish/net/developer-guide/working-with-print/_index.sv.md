---
title: Arbeta med Print
type: docs
weight: 80
url: /sv/net/working-with-print/
description: Det här avsnittet förklarar hur du skriver ut ett dokument via XPsPrint med Aspose.Diagram.
---
## **Hur man skriver ut ett dokument på en server via XPsPrint API**
Den här artikeln kan vara användbar för alla som vill skicka ett XPS-dokument till den ohanterade XPsPrint API från en .NET-applikation. Men huvudmålet om den här artikeln är att visa hur man skriver ut en diagram från en ASP.NET- eller Windows-tjänstapplikation med Aspose.Diagram och XPsPrint API.
### **Problem**
När du utvecklar en .NET-applikation och du behöver producera en del utskriven utskrift kan du använda klasserna i System.Drawing.Printing-namnområdet eller WPF-klasserna. Men, som det visar sig, om du utvecklar en ASP.NET eller Windows Serviceapplikation är dina utskriftsmöjligheter kraftigt begränsade, eftersom Microsoft rekommenderar att du inte använder dessa metoder. Se länkarna nedan för mer information.

<http://support.microsoft.com/kb/324565>

Användningen av .NET Framework utskriftsklasser stöds inte från en tjänst. Detta inkluderar ASP-sidor, som vanligtvis körs i samband med servertjänsten.

<http://msdn.microsoft.com/en-us/library/system.drawing.printing.aspx>

Klasser inom namnområdet System.Drawing.Printing stöds inte för användning inom en Windows-tjänst eller ASP.NET-applikation eller tjänst. Försök att använda dessa klasser från en av dessa programtyper kan orsaka oväntade problem, såsom försämrad tjänstprestanda och körtidsundantag.

<http://msdn.microsoft.com/en-us/library/bb613549.aspx>

Användningen av WPF för att bygga Windows-tjänster stöds inte. Eftersom WPF är en presentationsteknik kräver tjänsten Windows lämpliga behörigheter för att utföra visuella operationer som involverar användarinteraktion. Om tjänsten Windows inte har lämpliga behörigheter kan det bli oväntade resultat.

Dokumentobjektet tillhandahåller en familj av utskriftsmetoderna för att skriva ut dokument och dessa metoder skrivs ut via .NET-utskriftsklasserna definierade i System.Drawing.Printing-namnområdet. Det finns många kunder hos Aspose.Diagram som använder denna utskriftsmetod i sina applikationer på serversidan utan problem, men det finns ett sätt att följa Microsoft:s rekommendationer och det beskrivs i den här artikeln.
### **Lösning**
Det korrekta sättet att skriva ut dokument enligt Microsoft är att använda den ohanterade XpsPrint API. Denna API är tillgänglig på Windows 7, Windows Server 2008 R2 och även på 07611 Vista, 434 installerad på 07615.

Eftersom Aspose.Diagram enkelt kan konvertera vilket dokument som helst till XPS behöver vi bara skriva kod som skickar ett XPS-dokument till XPSPrint API. Det enda problemet är att XpsPrint API är ohanterat och det kräver viss kunskap om plattformsanropet.
### **Koden**
Vi har skapat klassen XpsPrintHelper med metoden Print, som är väldigt enkel att använda. Du behöver bara ange ett dokument som du vill skriva ut, ett skrivarnamn och ett valfritt jobbnamn. Om det var något problem med att skicka eller skriva ut dokumentet kommer metoden att skapa ett undantag.

Den sista parametern är ett booleskt värde som anger om koden ska vänta tills jobbet skrivs ut eller returneras direkt efter att utskriftsjobbet har skickats. Om du väljer att återvända omedelbart, kommer du inte att kunna avgöra om dokumentet har skrivits ut framgångsrikt eller inte i slutändan.
#### **Programmeringsexempel**
Följande kodexempel visar hur man anropar verktygsklassen för att skriva ut via XPS.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-PrintDiagramVisXPSPrinterAPI-PrintDiagramVisXPSPrinterAPI.cs" >}}


Det finns två överbelastningar av metoden XPsPrintHelper.Print. Den första överbelastningen tar ett Aspose.Diagram.Diagram-objekt och sparar det i en MemoryStream i XPS-formatet. Sedan anropar den den andra XpsPrintHelper.Print-överbelastningen.

Om du vill använda det här exemplet utan Aspose.Diagram (t.ex. du redan har ett XPS-dokument och bara vill skriva ut det från en ASP.NET eller Windows Service-applikation), så kan du bara ta bort den här metoden.
#### **XPS Stream och Skriv ut programmeringsexempel**
Detta kodexempel konverterar en Diagram till en XPS-ström och skriv ut.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-XpsPrintHelper-XpsPrint_PrintDocument.cs" >}}


Den andra XpsPrintHelper.Print-överbelastningen accepterar ett Stream-objekt. Strömmen måste innehålla ett dokument i XPS-format. Denna metod startar ett XPS-utskriftsjobb, skickar dokumentet till XPsPrint API och väntar sedan på resultatet om det behövs.
#### **XPsPrint API Programmeringsexempel**
Detta kodexempel skriver ut ett XPS-dokument med hjälp av XPsPrint API.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-XpsPrintHelper-XpsPrint_PrintStream.cs" >}}


Koden för metoderna StartJob, CopyJob, WaitForJob och CheckJobStatus samt definitioner av gränssnitten IXpsPrintJob och IXpsPrintJobStream är ganska låg nivå och använder Platform Invoke och COM Interop. Den här koden ingår inte i artikeln för korthetens skull, men den är tillgänglig i exempelnedladdningen.

XpsPrint API tillhandahåller också ytterligare funktionalitet, såsom att övervaka jobbets framsteg, men vår XpsPrintHelper är en mycket enkel inpackning och exponerar inte denna funktionalitet. Du kan lägga till detta själv om du vill.

{{% alert color="primary" %}}

När du kör projektet skrivs ett exempeldokument ut på den angivna skrivaren. För att göra resultaten synliga öppnas konsolfönstret. Programmet visar framgångsmeddelandet eller texten till ett undantag om ett sådant kastades.

{{% /alert %}}
## **Skriver ut en Diagram**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) tillhandahåller fyra överbelastningsmetoder för utskrift av diagrammen. Dessa metoder är tillräckligt flexibla för att skriva ut diagram till standardskrivaren eller till någon av de tillgängliga skrivarna med anpassade inställningar. Du behöver bara välja lämplig utskriftsmetod enligt kraven.
### **Skriver ut till standardskrivare**
Utskrift av diagram till standardskrivaren är ganska enkel i Aspose.Diagram for .NET. Utför följande steg för att skriva ut diagram till standardskrivaren:

- Skapa en instans av klassen Diagram för att ladda en diagram som ska skrivas ut
- Anropa utskriftsmetoden utan parametrar som exponeras av objektet Diagram
#### **Utskrift till standardskrivarprogrammeringsexempel**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-ByDefaultPrinter-ByDefaultPrinter.cs" >}}
### **Utskrift till specifik skrivare**
Utskrift av diagram till den specifika skrivaren kräver skrivarens namn som parameter för utskriftsmetoden för Diagram. Utför följande steg för att skriva ut diagram till önskad skrivare:

- Skapa en instans av klassen Diagram för att ladda en diagram som ska skrivas ut
- Anropa utskriftsmetoden för klassen Diagram med skrivarnamn som strängparameter till utskriftsmetoden
#### **Utskrift till specifik skrivarprogrammeringsexempel**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-BySpecificPrinter-BySpecificPrinter.cs" >}}
### **Ställa in skrivare och dokumentnamn**
Aspose.Diagram API:er gör det möjligt att ställa in det specifika skrivar- och dokumentnamnet för ett utskriftsjobb. Utför följande steg för att skriva ut diagram till önskad skrivare:

- Skapa en instans av klassen Diagram för att ladda en diagram som ska skrivas ut
- Anropa utskriftsmetoden för klassen Diagram med skrivare och dokumentnamn som strängparameter till utskriftsmetoden
#### **Inställning av skrivare och dokumentnamn Programmeringsexempel**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Print-SetPrintJobAndPrinterName-SetPrintJobAndPrinterName.cs" >}}
