---
title: Visio Makro Etkin diagram VBA kodlarını yönetin.
linktitle: Diagram VBA Projesi
type: docs
weight: 200
url: /tr/net/working-with-vbaproject/
description: Aspose.Diagram kitaplığı ile VBA Modülü ekleyin ve VBA veya Makroyu Değiştirin.
---
## **Bir VBA Modülü Ekleyin**
{{% alert color="primary" %}}

 Aspose.Diagram, Aspose.Diagram'i kullanarak yeni bir VBA Modülü ve Makro Kodu eklemenizi sağlar. Lütfen[**Diagram.VbaProject.Modules.Add()**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbamodulecollection/methods/add/index) diagram içine yeni VBA Modülü ekleme yöntemi

{{% /alert %}}

 Aşağıdaki örnek kod, yeni bir VBA Modülü ve Makro Kodu ekler ve çıktıyı VSDM biçiminde kaydeder. Bir kez, Microsoft Visio'de VSDM çıktı dosyasını açacaksınız ve**Geliştirici > Visual Basic** menü komutları, "TestModule" adında bir modül göreceksiniz ve içinde aşağıdaki makro kodunu göreceksiniz.

{{< highlight "java" >}}

 Sub ShowMessage()

    MsgBox "Welcome to Aspose!"

End Sub

{{< /highlight >}}

İşte VSDM çıktı dosyasını VBA Modülü ve Makro Kodu ile oluşturmak için örnek kod.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-Vba-AddModule.cs" >}}

## **VBA veya Makroyu Değiştirin**

{{% alert color="primary" %}} 

Aspose.Diagram'i kullanarak VBA veya Makro Kodunu değiştirebilirsiniz. Aspose.Diagram, Visio dosyasındaki VBA projesini okumak ve değiştirmek için aşağıdaki ad alanını ve sınıfları ekledi.

- Aspose.Diagram.Vba
- Vba Projesi
- VbaModül Koleksiyonu
- Vba Modülü

Bu makale, Aspose.Diagram kullanarak kaynak Visio dosyası içindeki VBA veya Makro Kodunu nasıl değiştireceğinizi gösterecektir.

{{% /alert %}} 

Aşağıdaki örnek kod, içinde aşağıdaki VBA veya Makro kodu bulunan kaynak Visio dosyasını yükler.

{{< highlight "java" >}}

 Sub Button1_Click()

    MsgBox "This is test message."

End Sub

{{< /highlight >}}

Aspose.Diagram örnek kodunun yürütülmesinden sonra, VBA veya Makro kodu bu şekilde değiştirilecektir.

{{< highlight "java" >}}

 Sub Button1_Click()

    MsgBox "This is Aspose.Diagram message."

End Sub

{{< /highlight >}}

 indirebilirsiniz[kaynak Visio dosyası]() ve[çıktı Visio dosyası]() verilen linklerden

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-Vba-ModifyModule.cs" >}}

## **ileri konular**
- [VBA Kodunun İmzalanıp İmzalanmadığını Kontrol Edin](/diagram/tr/net/check-if-vba-code-is-signed/)
