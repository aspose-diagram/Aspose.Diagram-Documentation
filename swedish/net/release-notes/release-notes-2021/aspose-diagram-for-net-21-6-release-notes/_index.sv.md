---
title: Aspose.Diagram for .NET 21.6 Release Notes
type: docs
weight: 7
url: /sv/net/aspose-diagram-for-net-21-6-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller information om release notes för Aspose.Diagram for .NET 21.6.

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-52007|Prestanda under initieringen av ett diagram-objekt|Förbättring|
|DIAGRAMNET-52008|Prestanda under initieringen av ett diagram-objekt|Förbättring|
|DIAGRAMNET-52027|Kvaliteten på former är inte bra i exporterad SVG-fil|Förbättring|
|DIAGRAMNET-52033|Problem med att spara former till HTML|Insekt|
|DIAGRAMNET-52035|"Oundantaget eof." undantag när filen VSDX är öppen|Insekt|
|DIAGRAMNET-52041|Det gick inte att spara vissa former från VSS-filen|Insekt|
|DIAGRAMNET-52042|"Parametern är inte giltig." undantag när VSD-filen renderas till HTML|Insekt|
|DIAGRAMNET-52043|"Objektreferens inte satt till en instans av ett objekt." undantag när du sparar form från filen VSSX|Insekt|

## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över alla ändringar som gjorts för allmänheten API, såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring som anges, vänligen ta upp den på supportforumet Aspose.Diagram.
### **Lade till EmfRenderSetting i SVGSaveOptions**
- Inställning för rendering av Emf-metafil

{{< highlight "java" >}}

SVGSaveOptions o = new SVGSaveOptions();
o.EmfRenderSetting = Aspose.Diagram.EmfRenderSetting.EmfPlusPrefer;

{{< /highlight >}}
### **Lägger till InheritTextBlock i Shape**
- Innehåller textblockvärdena för formen som ärvs av den överordnade stilen och huvudformen.



{{< highlight "java" >}}

shape.InheritTextBlock

{{< /highlight >}}





