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
**VSDX, VSD, VSDM, VSS, VSSX, VSSM, VTX, VSTM, VDX, VDW, VST, VSTX ve VSX**

diagram sınıfının yapıcıları ayrıca LoadFileFormat veya LoadOptions'ı tanımlayan isteğe bağlı bir parametre sunar. Geliştiricilerin Aspose.Diagram API'e iletebilecekleri ön yükleme bilgisidir. İdeal bir performans elde etmek için gerçekçi bilgileri iletmenizi öneririz.
## **Okuma Diagram Programlama Örneği**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Load-Save-Convert-ReadVisioDiagram-ReadVisioDiagram.cs" >}}
