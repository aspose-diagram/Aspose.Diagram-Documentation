---
title: Arbeta med användardefinierade celler
type: docs
weight: 150
url: /sv/net/working-with-user-defined-cells/
description: Det här avsnittet förklarar hur man läser användardefinierade celler i formerna visio med Aspose.Diagram.
---
## **Läs användardefinierade celler i Visio-formerna**
 Användare infogar textfält i former för att visa ytterligare information.**Användardefinierade celler** är den ena grenen av dessa fält och den här grenen använder information som anges i värdecellen i avsnittet Användardefinierade celler i formens ShapeSheet. Utvecklare kan infoga och läsa alla användardefinierade celler med hjälp av[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/).
### **Hämta de användardefinierade cellfälten**
 Användare samling exponerad av[Form](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) klass stöder objektet Aspose.Diagram.User. Den här egenskapen kan användas för att läsa de användardefinierade cellerna i en Visio-form som är tillgänglig i avsnittet Användardefinierade celler i formens ShapeSheet.

![todo:image_alt_text](working-with-user-defined-cells_1.png)
#### **Hämta cellprogrammeringsexempel**
Följande kodbit låter utvecklare läsa de användardefinierade cellfälten.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-User-defined-Cells-ReadUserdefinedCellsOfShape-ReadUserdefinedCellsOfShape.cs" >}}


Den här bilden visar utdata efter att ha kört ovanstående kod:

![todo:image_alt_text](working-with-user-defined-cells_2.png)
## **Skapa användardefinierad cell i ShapeSheet**
[Aspose.Diagram for .NET API](https://products.aspose.com/diagram/net/) gör det möjligt att skapa användardefinierad cell i formbladet. Det här exemplet beskriver hur utvecklare kan lägga till så många User.name-rader som de behöver, tilldela meningsfulla namn till raderna och ange cellvärden.
### **Skapa användardefinierad cell**
Add-metoden som exponeras av Users Collection kan användas för att skapa en användardefinierad cell i formarket. Det krävs en enda parameter.
#### **Skapa cellprogrammeringsexempel**
Använd följande kodexempel i din .NET-applikation för att skapa användardefinierad cell i formarket med Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-User-defined-Cells-CreateUserDefinedCellInShapeSheet-CreateUserDefinedCellInShapeSheet.cs" >}}
## **Hämta användardefinierade celler från Shapesheet**
Aspose.Diagram for .NET API gör det möjligt att hämta användardefinierade celler från formblad. Detta exempelämne beskriver hur utvecklare kan hämta alla User.name för alla former i en ritning.
### **Hämta användardefinierade celler**
Egenskaperna NameU, Value.Val och Prompt.Value som exponeras av klassen User kan användas för att hämta användardefinierade celler från formblad.
#### **Hämta celler från Shapesheet-programmeringsexempel**
Använd följande kod i din .NET-applikation för att hämta alla användardefinierade celler från formblad med Aspose.Diagram for .NET.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-User-defined-Cells-RetrieveUserDefinedCells-RetrieveUserDefinedCells.cs" >}}
