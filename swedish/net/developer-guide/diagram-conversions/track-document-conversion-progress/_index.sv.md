---
title: Spåra dokumentkonverteringsförlopp
type: docs
weight: 970
url: /sv/net/track-document-conversion-progress/
description: Det här avsnittet förklarar hur du spårar konverteringsförloppet för visio-filer med Aspose.Diagram.
---
## **Möjliga användningsscenarier**

 Ibland kan det ta lite tid att konvertera stora visio-filer. Under denna tid kanske du vill visa dokumentkonverteringsförloppet istället för bara en laddningsskärm för att förbättra användbarheten av din applikation. Aspose.Diagram stöder konverteringsprocess för spårning av dokument genom att tillhandahålla**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)** gränssnitt. De**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)**gränssnitt ger**[PageStartSaving](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback/methods/pagestartsaving)**och**[PageEndSaving](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback/methods/pageendsaving)**metoder som du kan implementera i din anpassade klass. Du kan också styra vilka sidor som renderas som visas i T*estDiagramPageSavingCallback*anpassad klass.

## **Spåra dokumentkonverteringsförlopp**

 Följande kodexempel laddar[källfil visio](Drawing1.vsdx) och skriver ut dess konverteringsförlopp i konsolen med hjälp av*TestPageSavingCallback* anpassad klass som implementerar**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)**gränssnitt.

## **Exempelkod**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-DiagramConversions-DocumentConversionProgress-1.cs" >}}

Följande är koden för*TestDiagramPageSavingCallback*anpassad klass.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-DiagramConversions-DocumentConversionProgress-2.cs" >}}

## **Konsolutgång**

Börja spara sidindex 0 av sidorna 11</br>
Sluta spara sidindex 0 av sidorna 11</br>
Börja spara sidindex 1 av sidorna 11</br>
Avsluta att spara sidindex 1 av sidorna 11</br>
Börja spara sidindex 2 av sidorna 11</br>
Avsluta att spara sidindex 2 av sidorna 11</br>
Börja spara sidindex 3 av sidorna 11</br>
Avsluta att spara sidindex 3 av sidorna 11</br>
Börja spara sidindex 4 av sidorna 11</br>
Avsluta att spara sidindex 4 av sidorna 11</br>
Börja spara sidindex 5 av sidorna 11</br>
Avsluta att spara sidindex 5 av sidorna 11</br>
Börja spara sidindex 6 av sidorna 11</br>
Avsluta att spara sidindex 6 av sidorna 11</br>
Börja spara sidindex 7 av sidorna 11</br>
Avsluta att spara sidindex 7 av sidorna 11</br>
Börja spara sidindex 8 av sidorna 11</br>
Avsluta att spara sidindex 8 av sidorna 11
