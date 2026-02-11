---
title: Şekiller Paragrafıyla Çalışma
type: docs
weight: 40
url: /tr/java/working-with-shapes-paragraph/
---
Aşağıdaki kod nasıl yapılacağını gösterir:

1. Bir örnek dosya yükleyin.
1. Belirli bir şekle erişin.
1. Şeklin paragrafını ayarlayın.
#### **Şeklin Paragraf Programlama Örneğinin Ayarlanması**
Java uygulamanızda aşağıdaki kodu kullanarak şeklin paragrafını Aspose.Diagram for Java kullanarak ayarlayın.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CreateNewVisio.class);
// initialize a Diagram class
Diagram diagram = new Diagram();

// save diagram in the VSDX format
diagram.save(dataDir + "CreateNewVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```