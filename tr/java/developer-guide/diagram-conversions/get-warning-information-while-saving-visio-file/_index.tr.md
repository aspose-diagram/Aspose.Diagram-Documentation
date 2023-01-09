---
title: Visio Dosyasını Kaydederken Uyarı Bilgisi Alın
type: docs
weight: 110
url: /tr/java/get-warning-information-while-saving-visio-file/
---
## **Olası Kullanım Senaryoları**

 Bazen kullanıcı, yerel yazı tipi olmayan metin içeren diagram'i kaydetmeye çalışır. Böyle bir durumda Aspose.Diagram diagram'i kaydederken uyarılar atar. Bu uyarıları aşağıdaki komutu uygulayarak yakalayabilirsiniz.**[IWarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback)** arayüz ve ayar**[SaveOptions.WarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/saveoptions/properties/warningcallback)**Emlak.

## **Visio Dosyasını Kaydederken Uyarı Alın**

 Aşağıdaki örnek kod, visio dosyasını kaydederken uyarıların nasıl alınacağını açıklar. kod dönüştürmek[örnek visio dosyası](sampleFontSubstitution.vsdx) hangi atar**[FontSubstitution](https://reference.aspose.com/diagram/net/aspose.diagram/warningtype)** kaydetme uyarısı. Bu uyarı daha sonra tarafından yakalanır**[IWarningCallback.Warning()](https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback/methods/warning)**konsoldaki uyarı mesajlarını yazdıran yöntem. Lütfen daha iyi anlamak için aşağıda verilen kodun konsol çıktısını da kontrol edin.

## **Basit kod**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-DiagramConversions-GetWarningInformation.cs" >}}

## **Konsol Çıkışı**

Sağlanan ile çalıştırıldığında yukarıdaki kodun konsol çıktısı aşağıdadır.[örnek visio dosyası](sampleFontSubstitution.vsdx).

{{< highlight "java" >}}
Font substitution: Font [ Athene Logos ]has been substituted by Font[Times New Roman]{{< /highlight >}}
