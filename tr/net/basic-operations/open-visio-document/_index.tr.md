---
title: Visio belgesini programlı olarak aç
linktitle: Visio belgesini aç
type: docs
weight: 20
url: /tr/net/open-visio-document/
description: Bu sayfada Visio belgesinin Aspose.Diagram kitaplığı ile sıfırdan nasıl açılacağı anlatılmaktadır.
---
## **Mevcut bir Visio Çizimini Okuyun**
Aspose.Diagram API, yeni Visio diyagramlarının sıfırdan oluşturulmasını ve ardından desteklenen herhangi bir dosya biçiminde kaydedilmesini destekler. Geliştiriciler ayrıca değişiklik, ekleme veya işleme amacıyla mevcut bir Visio diagram yükleyebilirler.
## **Diagram okunuyor**
Geliştiriciler, Aspose.Diagram API'i kullanarak desteklenen tüm Visio dosya biçimlerini yükleyebilir. Diagram sınıfının mevcut oluşturucuları buna izin verir ve geçerli bir dosya yolu dizesini veya kaynak Visio dosyasının dosya akışını kabul eder.

Desteklenen okunabilir dosya biçimleri aşağıdaki gibidir:
**VSDX, VSD, VSDM, VSS, VSSX, VSSM, VTX, VSTM, VDX, VDW, VST, VSTX ve 078111034**

diagram sınıfının yapıcıları ayrıca LoadFileFormat veya LoadOptions'ı tanımlayan isteğe bağlı bir parametre sunar. Geliştiricilerin Aspose.Diagram API'e iletebilecekleri ön yükleme bilgisidir. İdeal bir performans elde etmek için gerçekçi bilgileri iletmenizi öneririz.
## **Okuma Diagram Programlama Örneği**

{{< highlight csharp >}}
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

