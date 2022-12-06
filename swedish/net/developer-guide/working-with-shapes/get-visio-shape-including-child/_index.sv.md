---
title: Skaffa Visio Form inklusive barn
type: docs
weight: 110
url: /sv/net/get-visio-shape-including-child/
description: Det här avsnittet förklarar hur du får formen visio inklusive barn med formens id eller namn med Aspose.Diagram.
---
### **Hämta en Visio Shape inklusive barn**
Varje form i en diagram har ett ID och ett namn. ID:t är viktigt vid programmering med Visio: det är huvudmetoden för att komma åt en form. Varje form behåller också information om vilken master (stencil) den är gjord av.

 A[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) är ett föremål i en Visio-ritning som möjligen har en far eller söner. Shapes-egenskapen, exponerad av klassen Page, stöder en samling Aspose.Diagram.Shape-objekt. Egenskapen Shapes kan användas för att hämta information om en form.
#### **Hämta Visio Formprogrammeringsexempel**
Följande kodavsnitt hämtar formen inklusive barn. Kontrollera denna exempelkod:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-GetShapeIncludingChild-GetShapeIncludingChild.cs" >}}

