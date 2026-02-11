---
title: Visio Makro Etkin diagram VBA kodlarını yönetin.
linktitle: Diagram VBA Projesi
type: docs
weight: 200
url: /tr/java/working-with-vbaproject/
description: Aspose.Diagram kitaplığı ile VBA Modülü ekleyin ve VBA veya Makroyu Değiştirin.
---
## **Bir VBA Modülü Ekleyin**
{{% alert color="primary" %}}

Aspose.Diagram, Aspose.Diagram'i kullanarak yeni bir VBA Modülü ve Makro Kodu eklemenizi sağlar. Lütfen diagram içine yeni VBA Modülü eklemek için [**Diagram.VbaProject.Modules.Add()**] yöntemini kullanın.

{{% /alert %}}

 Aşağıdaki örnek kod, yeni bir VBA Modülü ve Makro Kodu ekler ve çıktıyı VSDM biçiminde kaydeder. Bir kez, Microsoft Visio'de VSDM çıktı dosyasını açacaksınız ve**Geliştirici > Visual Basic** menü komutları, "TestModule" adında bir modül göreceksiniz ve içinde aşağıdaki makro kodunu göreceksiniz.

{{< highlight "java" >}}

 Sub ShowMessage()

    MsgBox "Welcome to Aspose!"

End Sub

{{< /highlight >}}

İşte VSDM çıktı dosyasını VBA Modülü ve Makro Kodu ile oluşturmak için örnek kod.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
//Add module
int index = diagram.getVbaProject().getModules().add(VbaModuleType.PROCEDURAL, "TestModule");
//Get module 
com.aspose.diagram.VbaModule module = diagram.getVbaProject().getModules().get(index);
//Set module
module.setCodes("Attribute VB_Name = \"module2\"\r\n Sub Button1_Click()\r\n\r\n    MsgBox \"Welcome to Aspose!\"\r\n\r\nEnd Sub\r\n");

diagram.save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

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

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
//Get module 
com.aspose.diagram.VbaModule module = diagram.getVbaProject().getModules().get(2);
//Set module
module.setCodes("Attribute VB_Name = \"module2\"\r\n Sub Button1_Click()\r\n\r\n    MsgBox \"This is Aspose.Diagram message.\"\r\n\r\nEnd Sub\r\n");

diagram.save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

## **ileri konular**
- [VBA Kodunun İmzalanıp İmzalanmadığını Kontrol Edin](/diagram/tr/java/check-if-vba-code-is-signed/)
