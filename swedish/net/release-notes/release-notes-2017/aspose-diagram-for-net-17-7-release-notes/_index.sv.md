---
title: Aspose.Diagram for .NET 17.7 Release Notes
type: docs
weight: 60
url: /sv/net/aspose-diagram-for-net-17-7-release-notes/
---
{{% alert color="primary" %}} 

 Den här sidan innehåller release notes för[Aspose.Diagram for .NET 17.7](https://www.nuget.org/packages/Aspose.Diagram/17.7.0).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|DIAGRAMNET-51204|Skrivarens pappersstorlek ändras efter diagram sparande.|Förbättring|
|DIAGRAMNET-51230|Felaktiga värden på sidmarginalerna.|Förbättring|
|DIAGRAMNET-51274|Lägg till stöd för att infoga kommentarer på formnivån.|Förbättring|
|DIAGRAMNET-51297|Ingång VDX - felaktig läsning av SolutionXML.|Förbättring|
|DIAGRAMNET-51061|Saknade former vid konvertering av en VST till PNG.|Insekt|
|DIAGRAMNET-51262|Förskjutna textobjekt vid konvertering av en VSDM till SVG.|Insekt|
|DIAGRAMNET-51276|VSD till SVG - alla ikoner syns inte korrekt.|Insekt|
|DIAGRAMNET-51277|VSDM till SVG - Skugga av former saknas.|Insekt|
|DIAGRAMNET-51279|Ett saknat tecken vid konvertering av en VSD till PDF.|Insekt|
|DIAGRAMNET-51282|Vissa vdx-filer är skadade efter att ha sparats.|Insekt|
|DIAGRAMNET-51284-|DiagramException inträffar vid vsdx filladdning.|Insekt|
|DIAGRAMNET-51285|VSD till PNG - alla textobjekt saknas.|Insekt|
|DIAGRAMNET-51286|VSD till PNG - den partiella återgivningen av en form.|Insekt|
|DIAGRAMNET-51288|Fel i ogiltigt färgvärde vid konvertering av en VSDX till PNG.|Insekt|
|DIAGRAMNET-51289|Ikonen för kommentarer på sidnivå visar inte text.|Insekt|
|DIAGRAMNET-51290|Aspose.Diagram bugg i metoden SetWidth.|Insekt|
|DIAGRAMNET-51291|Utgång VSDX - felaktig layout vid raka anslutningslinjer.|Insekt|
|DIAGRAMNET-51292|Utdata VSDX - textposten för anslutande linjer är felplacerad.|Insekt|
|DIAGRAMNET-51293|VSDX till SVG - ytterligare ett märke visas tillsammans med former.|Insekt|
|DIAGRAMNET-51294|VSDM till SVG - ytterligare ett märke visas tillsammans med former.|Insekt|
## **Offentlig API och bakåtinkompatibla ändringar**
Följande är en lista över eventuella ändringar som gjorts för allmänheten API, t.ex. tillagda, bytt namn, borttagna eller utfasade medlemmar samt alla icke-bakåtkompatibla ändringar som gjorts till Aspose.Diagram for .NET. Om du har frågor om någon ändring i listan, vänligen ta upp dem i de[Aspose.Diagram supportforum](https://forum.aspose.com/c/diagram/17).
### **AddComment Method läggs till i klassen Page**
En överbelastad AddComment-metod, som exponeras av klassen Page, tar en Shape-klassinstans och textsträng av kommentaren.

{{< highlight "java" >}}

 // load diagram

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

// retrieve page by name

Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

// retrieve shape by ID

Aspose.Diagram.Shape shape = page.Shapes.GetShape(12);

page.AddComment(shape, "Hello");

// save diagram

diagram.Save(@"c:\temp\Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **Användningsexempel**
Kontrollera listan med hjälpämnen som lagts till i Aspose.Diagram Wiki-dokument:

1. [Lägg till en kommentar på formnivå i Visio Ritning](/diagram/sv/net/working-with-comments/#workingwithcomments-addashape-levelcommentinvisiodrawing)
