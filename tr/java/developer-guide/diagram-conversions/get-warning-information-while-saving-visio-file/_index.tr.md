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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Intro();

// call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "sampleFontSubstitution.vsdx");

// create an instance SVG save options class
Aspose.Diagram.Saving.SVGSaveOptions so = new Aspose.Diagram.Saving.SVGSaveOptions();

so.WarningCallback = new TestDiagramWarningCallback();
// save Visio drawing
diagram.Save(dataDir + "WarningCallback_out.svg", options);


public class TestDiagramWarningCallback : Aspose.Diagram.IWarningCallback
{
    public void Warning(Aspose.Diagram.WarningInfo info)
    {
        if (info.WarningType == Aspose.Diagram.WarningType.FontSubstitution)
        {
            Console.WriteLine("Diagram WARNING INFO: " + info.Description);
        }

    }
}

{{< /highlight >}}


## **Konsol Çıkışı**

Sağlanan ile çalıştırıldığında yukarıdaki kodun konsol çıktısı aşağıdadır.[örnek visio dosyası](sampleFontSubstitution.vsdx).

{{< highlight "java" >}}
Font substitution: Font [ Athene Logos ]has been substituted by Font[Times New Roman]{{< /highlight >}}
