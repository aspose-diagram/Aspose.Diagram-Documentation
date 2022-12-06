---
title: Hur man kör exemplen
type: docs
weight: 80
url: /sv/net/how-to-run-the-examples/
description: Den här sidan beskriver hur du kör exemplen på Aspose.Diagram-biblioteket.
---
## **Programvarukrav**
Se till att du uppfyller följande krav innan du laddar ner och kör exemplen.

1. Visual Studio 2010 eller senare
1. Microsoft office visio
1.  NuGet Package Manager installerad i Visual Studio. Se till att senaste versionen NuGet API är installerad i Visual Studio. För detaljer om hur du installerar NuGet pakethanterare, kontrollera<http://docs.nuget.org/ndocs/guides/install-nuget>
1.  Gå till Verktyg->Alternativ->NuGet Pakethanterare->Paketkällor och se till att alternativet**nuget.org** är kontrollerad
1.  Exempelprojekt använder NuGet funktionen Automatisk paketåterställning, därför bör du ha en aktiv internetanslutning. Om du inte har en aktiv internetanslutning på maskinen där exempel ska utföras, kontrollera[Installation](/diagram/sv/net/installation/) och manuellt lägg till referens till Aspose.Diagram.dll i exempelprojektet.
## **Ladda ner från GitHub**
 Alla exempel på Aspose.Diagram for .NET finns på[GitHub](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET).

-  Du kan antingen klona förvaret med din favorit GitHub-klient eller ladda ner ZIP-filen från[här](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/archive/master.zip).
-  Extrahera innehållet i ZIP-filen till valfri mapp på din dator. Alla exempel finns i**Exempel** mapp.
- Det finns en Visual Studio-lösningsfil för C#.
- Projekten skapas i Visual Studio 2013, men lösningsfilen är kompatibel med Visual Studio 2010 SP1 och högre.
- Öppna lösningsfilen i Visual Studio och bygg projektet.
- Vid första körningen kommer beroenden automatiskt att laddas ner via NuGet.
- **Data** mapp i rotmappen för**Exempel** innehåller indatafiler som CSharp-exempel använder. Det är obligatoriskt att ladda ner**Data** mapp tillsammans med exempelprojektet.
- Öppna RunExamples.cs; alla exempel kallas härifrån.
- Avkommentera de exempel du vill köra inifrån projektet.

Kontakta gärna våra forum om du har problem med att installera eller köra exemplen.
## **Bidra**
Om du vill lägga till eller förbättra ett exempel uppmuntrar vi dig att bidra till projektet. Alla exempel och utställningsprojekt i det här arkivet är öppen källkod och kan fritt användas i dina egna applikationer.

För att bidra kan du dela förvaret, redigera källkoden och skapa en pull-begäran. Vi kommer att granska ändringarna och inkludera dem i arkivet om det är användbart.
