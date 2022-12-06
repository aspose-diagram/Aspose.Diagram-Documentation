---
title: Olika sätt att öppna filer
type: docs
weight: 10
url: /sv/python-net/different-ways-to-open-files/
---
{{% alert color="primary" %}}

Med Aspose.Diagram är det enkelt att öppna filer, till exempel för att hämta data, eller att använda en designermall för att påskynda utvecklingsprocessen.

{{% /alert %}}

## **Öppna en fil via en sökväg**

 Utvecklare kan öppna en Microsoft Diagram fil med hjälp av dess sökväg på den lokala datorn genom att ange den i**Diagram**klass konstruktör. Passera helt enkelt vägen i konstruktorn som en*sträng*. Aspose.Diagram kommer automatiskt att upptäcka filformatstypen.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaPath.py" >}}

## **Öppna en fil via en ström**

 Det är också enkelt att öppna en Visio-fil som en stream. För att göra det, använd en överbelastad version av konstruktorn som tar*BufferStream*objekt som innehåller filen.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaStream.py" >}}

## **Öppna en fil med LoadOptions**

 För att öppna en fil med laddningsalternativ, använd**LoadOptions**klasser för att ställa in relaterade alternativ för klasserna för mallfilen som ska laddas.

{{< gist "aspose-diagram-gists" "ba6a69bbbb0ec99f2a0561b49bcd96e7" "Examples-PythonNet-OpenFileViaLoadOptions.py" >}}

