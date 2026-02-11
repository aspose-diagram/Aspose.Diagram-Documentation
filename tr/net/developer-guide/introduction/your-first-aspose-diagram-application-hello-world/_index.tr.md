---
title: İlk Başvurunuz Aspose.Diagram - Hello World
type: docs
weight: 30
url: /tr/net/your-first-aspose-diagram-application-hello-world/
description: Bu sayfada Aspose.Diagram kitaplığı ile ilk uygulamanın nasıl oluşturulacağı açıklanmaktadır.
---
{{% alert color="primary" %}}

Bu öğretici, Aspose.Diagram' basit API'i kullanarak ilk uygulamanın (Hello World) nasıl oluşturulacağını gösterir. Bu basit uygulama, belirli bir Sayfada 'Hello World' metniyle bir Microsoft Visio dosyası oluşturur.

{{% /alert %}}

## **Hello World Uygulamasını Oluşturma**

Aşağıdaki adımlar, Aspose.Diagram API'i kullanarak Hello World uygulamasını oluşturur:

1.  örneğini oluşturun[Diagram](https://reference.aspose.com/diagram/net/aspose.diagram/diagram) sınıf.
1.  Ehliyetin varsa o zaman[uygula](https://reference.aspose.com/diagram/net/aspose.diagram/license).
 Değerlendirme sürümünü kullanıyorsanız, lisansla ilgili kod satırlarını atlayın.
1. Yeni bir Visio dosyası oluşturun veya mevcut bir Visio dosyasını açın.
1. Yeni bir metin kutusu oluşturun.
1.  kelimeleri ekle**Hello World!** bir metin kutusuna.
1. Değiştirilen Microsoft Visio dosyasını oluşturun.

Yukarıdaki adımların uygulanması aşağıdaki örneklerde gösterilmektedir.

### **Kod Örneği: Yeni Bir Diagram Oluşturma**

Aşağıdaki örnek sıfırdan yeni bir diagram oluşturur, Hello World yazar! ilk sayfada ve Visio dosyasını kaydeder.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Initialize a Diagram class
Diagram diagram = new Diagram();

// Save diagram in the VSDX format
diagram.Save(dataDir + "CreateNewVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

### **Kod Örneği: Mevcut Bir Dosyayı Açma**

Aşağıdaki örnek, "Sample.vsdx" adlı mevcut bir Microsoft Visio şablon dosyasını açar, "Hello World!" girer. metni ilk sayfaya kaydeder ve diagram'i kaydeder.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD stream
FileStream st = new FileStream(dataDir + "Drawing1.vsdx", FileMode.Open);
Diagram vsdDiagram = new Diagram(st);
st.Close();

// Call the diagram constructor to load a VDX diagram
Diagram vdxDiagram = new Diagram(dataDir + "Drawing1.vdx");

/*
 * Call diagram constructor to load a VSS stencil
 * providing load file format
*/
Diagram vssDiagram = new Diagram(dataDir + "Basic.vss", LoadFileFormat.VSS);

/*
 * Call diagram constructor to load diagram from a VSX file
 * providing load options
*/
LoadOptions loadOptions = new LoadOptions(LoadFileFormat.VSX);
Diagram vsxDiagram = new Diagram(dataDir + "Drawing1.vsx", loadOptions);

{{< /highlight >}}
```
