---
title: Откройте существующий чертеж Visio в Ruby
type: docs
weight: 90
url: /ru/java/open-an-existing-visio-drawing-in-ruby/
---
## **Aspose.Diagram - Открытие существующего чертежа Visio**
 Чтобы открыть существующий чертеж Visio с помощью**Aspose.Diagram Java для рубина**, вы можете использовать следующий код.

**Рубиновый код**

{{< highlight "ruby" >}}

 data_dir = File.dirname(File.dirname(File.dirname(File.dirname(__FILE__)))) + '/data/'

\# Call the diagram constructor to load diagram from a VSD file

diagram = Rjb::import('com.aspose.diagram.Diagram').new(data_dir + "Drawing.vsd")

{{< /highlight >}}
