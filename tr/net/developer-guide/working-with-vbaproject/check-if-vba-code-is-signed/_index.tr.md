---
title: VBA Kodunun İmzalanıp İmzalanmadığını Kontrol Edin
type: docs
weight: 100
url: /tr/net/check-if-vba-code-is-signed/
description: vba kodunun Aspose.Diagram kitaplığı ile imzalanıp imzalanmadığını kontrol edin.
---
{{% alert color="primary" %}}

Aspose.Diagram, kullanıcının VBA kod projesinin imzalanıp imzalanmadığını kontrol etmesini sağlar. lütfen[**Diagram.VbaProject.IsSigned**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbaproject/properties/issigned) VBA kod projesinin imzalanıp imzalanmadığını kontrol etmek için özellik.

{{% /alert %}}

 Aşağıdaki kod, VBA kodunun imzalanıp imzalanmadığının nasıl kontrol edileceğini açıklar.[**Diagram.VbaProject.IsSigned**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbaproject/properties/issigned) Emlak. Bu kodu test etmek için visio dosyalarınızdan herhangi birini kullanabilirsiniz. Test amaçlı kullanabilirsiniz[kodda kullanılan bu visio dosyası](1.vsdm).

## Basit kod


{{< highlight csharp >}}

// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");

// Signature is valid
Console.WriteLine("Is VBA Code Project Signed: " + diagram.VbaProject.IsSigned);

diagram.Save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}


## Konsol Çıkışı

 Aşağıda, yukarıdaki kodun konsol çıktısını kullanarak[örnek visio dosyası](1out.vsdm) bağlantı ile sağlanır.

{{< highlight "java" >}}

Is VBA Code Project Signed: False

{{< /highlight >}}
