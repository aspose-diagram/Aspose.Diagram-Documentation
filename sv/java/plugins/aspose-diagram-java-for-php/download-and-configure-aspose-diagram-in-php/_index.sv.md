---
title: Ladda ner och konfigurera Aspose.Diagram i PHP
type: docs
weight: 10
url: /sv/java/download-and-configure-aspose-diagram-in-php/
---
## **Ladda ner obligatoriska bibliotek**
Ladda ner nödvändiga bibliotek som nämns nedan. Dessa är nödvändiga för att köra Aspose.Diagram Java för Ruby-exempel.

- [Aspose.Diagram for Java Komponent](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram)
## **Ladda ner exempel från webbplatser för social kodning**
Följande versioner av löpande exempel finns att ladda ner på nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/tree/master/Plugins/Aspose_Diagram_Java_for_PHP)
## **Installerar**
Det är mycket enkelt och lätt att installera Aspose.Diagram Java för PHP, följ instruktionerna:

Kör följande kommando.

{{< highlight "java" >}}

 $ gem install asposediagramjava

{{< /highlight >}}
## **Använder sig av**
Inkludera de nödvändiga filerna för att exportera visio-ritningen till PDF-dokument.

{{< highlight "java" >}}

 require File.dirname(File.dirname(File.dirname(__FILE__))) + '/lib/asposediagramjava'

include Asposediagramjava

include Asposediagramjava::ExportToPdf

initialize_aspose_Diagram

{{< /highlight >}}

Låt oss förstå koden ovan.

1. Den första raden ser till att Aspose.Diagram är laddad och tillgänglig.
1. Inkludera filerna som krävs för att komma åt Aspose.Diagram
1. Initiera biblioteken. Aspose Java-klasserna laddas från sökvägen i filen aspose.yml
