---
title: Aspose.Diagram for .NET 19.8 Release Notes
type: docs
weight: 50
url: /sv/net/aspose-diagram-for-net-19-8-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller release notes för[Aspose.Diagram for .NET 19.8](https://www.nuget.org/packages/Aspose.Diagram/19.8.0)

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-50334|Lägg till stöd för VBA-koder / makron (lägg till - redigera - ta bort)|Förbättring|
|DIAGRAMNET-51083|Lägg till stöd för att rita Spline|Förbättring|
|DIAGRAMNET-51676|Visio till HTML - utdata innehåller filnamnet|Förbättring|
|DIAGRAMNET-50263|Det går inte att ange plats för anslutningstext som formler|Insekt|
|DIAGRAMNET-50284|VTX till HTML-konvertering, formernas fyllnadsfärg bevaras inte|Insekt|
|DIAGRAMNET-50432|VDX till PDF-konvertering, Diagram.setFontDirs-metoden använder endast första teckensnittet över hela diagram|Insekt|
|DIAGRAMNET-50463|VSDX till PDF-konvertering, saknade eller ofullständiga formrendering|Insekt|
|DIAGRAMNET-51033|Nätverksformerna bevaras inte vid konvertering av en VSDX till PDF|Insekt|
|DIAGRAMNET-51303|VSDX till PDF - färgen på text på anslutande linjer ändras|Insekt|
|DIAGRAMNET-51663|Ett ohanterat undantag inträffar vid konvertering av VSD till VSDX|Insekt|
|DIAGRAMNET-51664|Filen blir skadad efter att ett oanvänt tema tagits bort|Insekt|
|DIAGRAMNET-51665|Bilder visas som X efter att oanvända teman har tagits bort|Insekt|
|DIAGRAMNET-51667|När du tar bort stilar är det bara en bild som har problem|Insekt|
|DIAGRAMNET-51668|VISIO till JPG - utdatabilden är inte i rätt format|Insekt|
|DIAGRAMNET-51671|När du tar bort oanvända masterformer och stilar är det bara bilden som har ett problem|Insekt|
|DIAGRAMNET-51672|Förlorade bilder vid laddning och spara|Insekt|
|DIAGRAMNET-51677|Visio till HTML - Länk i genererad HTML fungerar inte|Insekt|
|DIAGRAMNET-51678|Visio till HTML - Datumformatet är felaktigt när du sparar som HTML|Insekt|
|DIAGRAMNET-51679|Visio till PDF - Flera formateringsfel i PDF|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över eventuella ändringar som gjorts för allmänheten API, t.ex. tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp dem i de[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
### **Lägger till DrawSpline i sidan**
Följande kodavsnitt visar hur man ritar spline:

{{< highlight "java" >}}

 PointF[]ps = new PointF[]{ new PointF(0, 0.3270758925347308f), 

                             new PointF(0.2926845121364643f, 0.3581517392187368f), 

                             new PointF(0.6526026522346893f, 0.4640748257705201f), 

                             new PointF(1f, 0.327075892534732f) };

                             diagram.Pages[0].DrawSpline(1, 1, 2, 2, ps);

{{< /highlight >}}
### **Lägger till SaveTitle i HTMLSaveOptions**
Följande kodavsnitt definierar om du vill spara titeln eller inte:

{{< highlight "java" >}}

 Aspose.Diagram.Saving.HTMLSaveOptions options = new Aspose.Diagram.Saving.HTMLSaveOptions();

options.SaveTitle = false;

{{< /highlight >}}




