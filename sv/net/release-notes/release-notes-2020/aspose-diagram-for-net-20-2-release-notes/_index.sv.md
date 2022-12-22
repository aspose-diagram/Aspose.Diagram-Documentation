---
title: Aspose.Diagram for .NET 20.2 Release Notes
type: docs
weight: 60
url: /sv/net/aspose-diagram-for-net-20-2-release-notes/
---
{{% alert color="primary" %}} 

Den här sidan innehåller information om release notes för Aspose.Diagram for .NET 20.2.

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51747|Filändringar efter Visio vsd->vsdx konvertering|Förbättring|
|DIAGRAMNET-51750|Lägger till flaggan "HasHiddenInfo"|Förbättring|
|DIAGRAMNET-51748|Lägg till PNG till Diagram - insynen är förlorad|Insekt|
|DIAGRAMNET-51749|Ett fel uppstår när Visio-dokumentet sparas|Insekt|
|DIAGRAMNET-51751|VSDX till PNG - Extra bild visas|Insekt|
|DIAGRAMNET-51752|VSDX till PNG - Extra utrymme visas|Insekt|
|DIAGRAMNET-51753|VSDX till PNG - Ikonernas position ändras|Insekt|
|DIAGRAMNET-51754|VSDX till PNG - Frågeteckens ikonposition har ändrats|Insekt|
|DIAGRAMNET-51762|PDF som genereras är annorlunda jämfört med ingången Visio diagram|Insekt|
|DIAGRAMNET-51763|VSDX till PNG - Information saknas i utgången|Insekt|
## ` `**Offentlig API och bakåtinkompatibla ändringar**
` `Följande är en lista över alla ändringar som gjorts för allmänheten API såsom tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp det på supportforumet Aspose.Diagram.
### **Lade till EnlargePage i ImageSaveOptions**
- Anger om sidan ska förstoras

{{< highlight "java" >}}

 Aspose.Diagram.Saving.ImageSaveOptions opt = new Aspose.Diagram.Saving.ImageSaveOptions(Aspose.Diagram.SaveFileFormat.PNG);

opt.EnlargePage = false;

{{< /highlight >}}
### **Lade till HasHiddenInfo i Diagram**
- Indikerar om denna diagram har dold information.



{{< highlight "java" >}}

 diagram.HasHiddenInfo();

{{< /highlight >}}




