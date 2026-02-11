---
title: Dosyaları Açmanın Farklı Yolları
type: docs
weight: 10
url: /tr/python-net/different-ways-to-open-files/
---
{{% alert color="primary" %}}

Aspose.Diagram ile dosyaları açmak, örneğin verileri almak veya geliştirme sürecini hızlandırmak için bir tasarımcı şablonu kullanmak kolaydır.

{{% /alert %}}

## **Dosya Açma via Yol**

 Geliştiriciler, yerel bilgisayardaki dosya yolunu kullanarak bir Microsoft Diagram dosyasını,**Diagram**sınıf oluşturucu Yapıcıdaki yolu basit bir şekilde iletin*sicim*. Aspose.Diagram, dosya biçimi türünü otomatik olarak algılar.


{{< highlight python >}}
import aspose.diagram
from aspose.diagram import *

#// Initialize a Diagram class
diagram = Diagram(os.path.join(sourceDir, "Drawing1.vsdx"))

#// Save diagram in the VSDX format
diagram.save("CreateNewVisio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


## **Dosya Açma via Akış**

 Bir Visio dosyasını akış olarak açmak da kolaydır. Bunu yapmak için, yapıcının aşırı yüklenmiş bir sürümünü kullanın.*Tampon Akışı*dosyayı içeren nesne.


{{< highlight python >}}
import os
import sys
import aspose.diagram
from aspose.diagram import *
from aspose.pyio import BufferStream

#// Build path of an existing diagram
visioDrawing = os.path.join(sourceDir, "Drawing1.vsdx")
# Create a Stream object
f = open(visioDrawing, 'rb')
data = f.read()
databuff = BufferStream(data)
diagram = Diagram(databuff)

#// Save diagram in the VSDX format
diagram.save("Visio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


## **LoadOptions ile Dosya Açma**

 Bir dosyayı loadoptions ile açmak için,**Yükleme Seçenekleri**yüklenecek şablon dosyası için sınıfların ilgili seçeneklerini ayarlamak için sınıflar.


{{< highlight python >}}
import os
import sys
import aspose.diagram
from aspose.diagram import *

#// Build path of an existing diagram
visioDrawing = os.path.join(sourceDir, "Drawing1.vsdx")
# Instantiate LoadOptions specified by the LoadFileFormat
loadOptions = LoadOptions(LoadFileFormat.VSDX)
diagram = Diagram(visioDrawing,loadOptions)

#// Save diagram in the VSDX format
diagram.save("Visio_out.vsdx", SaveFileFormat.VSDX)
{{< /highlight >}}


