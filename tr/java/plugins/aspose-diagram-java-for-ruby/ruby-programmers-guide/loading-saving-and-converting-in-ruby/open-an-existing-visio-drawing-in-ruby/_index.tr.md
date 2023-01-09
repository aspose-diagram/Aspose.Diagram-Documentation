---
title: Ruby'de Mevcut Bir Visio Çizimini Açın
type: docs
weight: 90
url: /tr/java/open-an-existing-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Mevcut bir Visio Çizimini açın**
 Kullanarak Mevcut Bir Visio Çizimini Açmak İçin**Yakut için Aspose.Diagram Java**, aşağıdaki kodu kullanabilirsiniz.

**Yakut Kodu**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

{{< /highlight >}}
