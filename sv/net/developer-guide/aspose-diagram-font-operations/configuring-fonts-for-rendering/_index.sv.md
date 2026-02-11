---
title: Konfigurera teckensnitt för rendering
type: docs
weight: 10
url: /sv/net/configuring-fonts-for-rendering/
---
## **Möjliga användningsscenarier**

Aspose.Diagram API:er ger möjlighet att rendera sidor i bildformat samt konvertera dem till PDF och XPS format. För att maximera omvandlingstroheten är det nödvändigt att teckensnitten som används i kalkylarket är tillgängliga i operativsystemets standardtypsnittskatalog. Om de nödvändiga typsnitten inte finns kommer API:erna Aspose.Diagram att försöka ersätta de nödvändiga typsnitten med de tillgängliga.

## **Val av teckensnitt**

Nedan är processen som Aspose.Diagram API:er följer bakom scenen.

1. API försöker hitta teckensnitten i filsystemet som matchar det exakta teckensnittsnamnet som används i kalkylarket.
1.  Om API inte kan hitta teckensnittet som definieras under**[SaveOptions.DefaultFont](https://reference.aspose.com/diagram/net/aspose.diagram.saving/saveoptions/defaultfont/)** egenskapen försöker den använda typsnittet som anges under**[FontConfigs.DefaultFontName](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/defaultfontname/)**fast egendom.
1.  Om API inte kan hitta teckensnittet som definieras under**[FontConfigs.DefaultFontName](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/defaultfontname/)** egenskapen försöker den välja de mest lämpliga typsnitten från alla tillgängliga typsnitt.
1. Slutligen, om API inte kan hitta några teckensnitt i filsystemet, renderar den sidan med Times New Roman.

## **Ställ in anpassade teckensnittsmappar**

 Aspose.Diagram API:er söker i operativsystemets standardtypsnittskatalog efter de nödvändiga teckensnitten. Om de nödvändiga typsnitten inte är tillgängliga i systemets teckensnittskatalog så söker API:erna igenom de anpassade (användardefinierade) katalogerna. De**[FontConfigs](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/)** class har avslöjat ett antal sätt att ställa in anpassade teckensnittskataloger som beskrivs nedan.

1. **[FontConfigs.SetFontFolder](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolder/)**: Den här metoden är användbar om det bara finns en mapp att ställa in.

1. **[FontConfigs.SetFontFolders](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolders/)**Den här metoden är användbar när teckensnitten finns i flera mappar och användaren vill ställa in alla mappar separat istället för att kombinera alla teckensnitt i en enda mapp.
1. **[FontConfigs.SetFontSources](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontsources/)**: Den här mekanismen är användbar när användaren vill ladda teckensnitt från flera mappar eller en enda teckensnittsfil eller teckensnittsdata från en uppsättning byte.

{{% alert color="primary" %}}

 Både**[FontConfigs.SetFontFolder](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolder/)** & **[FontConfigs.SetFontFolders](https://reference.aspose.com/diagram/net/aspose.diagram/fontconfigs/setfontfolders/)** metoder accepterar en andra parameter av boolesk typ. Godkänd**Sann** eftersom den andra parametern kommer att styra API:erna Aspose.Diagram att söka i undermapparna efter teckensnittsfilerna.

{{% /alert %}}

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// Load the Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

//Setting default font
Aspose.Diagram.FontConfigs.DefaultFontName = "Arial";
// Setting the custom font directories
Aspose.Diagram.FontConfigs.SetFontFolder(Environment.GetFolderPath(Environment.SpecialFolder.Fonts), false);

// Saving Visio diagram in PDF format
diagram.Save(dataDir + "Font.pdf", SaveFileFormat.PDF);

{{< /highlight >}}
```

{{% alert color="primary" %}}

Använd någon av de ovan nämnda metoderna i början av ansökan, det vill säga; innan du anropar några andra objekt i Aspose.Diagram API:er.

{{% /alert %}} {{% alert color="primary" %}}

Om alla ovan nämnda metoder används för att ställa in teckensnittskällorna, kommer endast de senaste inställningarna att träda i kraft.

{{% /alert %}}

