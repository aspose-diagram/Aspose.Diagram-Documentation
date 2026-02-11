---
title: VBA Kodunun İmzalanıp İmzalanmadığını Kontrol Edin
type: docs
weight: 100
url: /tr/java/check-if-vba-code-is-signed/
description: vba kodunun Aspose.Diagram kitaplığı ile imzalanıp imzalanmadığını kontrol edin.
---
{{% alert color="primary" %}}

Aspose.Diagram, kullanıcının VBA kod projesinin imzalanıp imzalanmadığını kontrol etmesini sağlar. VBA kod projesinin imzalanıp imzalanmadığını kontrol etmek için lütfen [**Diagram.VbaProject.IsSigned**] özelliğini kullanın.

{{% /alert %}}

 Aşağıdaki kod, [**Diagram.VbaProject.IsSigned**]özelliği kullanılarak VBA kodunun imzalanıp imzalanmadığının nasıl kontrol edileceğini açıklar. Bu kodu test etmek için visio dosyalarınızdan herhangi birini kullanabilirsiniz. Test amaçlı kullanabilirsiniz[kodda kullanılan bu visio dosyası](1.vsdm).

## Basit kod

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
  
//Check signed     
boolean isSigned = diagram.getVbaProject().isSigned();

diagram.save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

## Konsol Çıkışı

 Aşağıda, yukarıdaki kodun konsol çıktısını kullanarak[örnek visio dosyası](1out.vsdm) bağlantı ile sağlanır.

{{< highlight "java" >}}

Is VBA Code Project Signed: False

{{< /highlight >}}
