---
title: Hello World Örnek
type: docs
weight: 90
url: /tr/net/hello-world-example/
description: Bu sayfada, Aspose.Diagram kitaplığı ile merhaba dünya örneğinin nasıl oluşturulacağı açıklanmaktadır.
---
## **Hello World Örnek**
Aspose.Diagram for .NET, C# ve diğer .NET dillerini kullanarak Microsoft Visio dosyalarını oluşturmak, açmak, düzenlemek ve dönüştürmek için zengin özelliklere sahiptir. It supports a wide set of Visio file formats including VSDX, VDX, VSD, VSX, VTX, VSSX, VSDM, VSSM, VSTM, VDW, VSS, and VST. In addition, it provides the capability to convert Visio Diagrams to a number of PDF, HTML, XML, SVG ve XAML gibi biçimler.

Sonrasında[yükleme Aspose.Diagram for .NET](/diagram/tr/net/installation/)ortamınızda, Aspose.Diagram API'in .NET uygulamalarında nasıl kullanıldığını görmek için aşağıdaki adımlar kullanılabilir.

1. Bir Diagram nesnesini somutlaştırın
1. Dosyayı diske kaydetmek için Diagram sınıf nesnesinin Kaydetme yöntemini kullanın

Aşağıdaki kod parçacığı, Aspose.Diagram for .NET API'in çalışmasını gösteren bir Hello World programıdır.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Initialize a Diagram class
Diagram diagram = new Diagram();

// Save diagram in the VSDX format
diagram.Save(dataDir + "CreateNewVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}





