---
title: Temalarla Çalışmak
type: docs
weight: 265
url: /tr/net/working-with-themes/
description: Bu bölümde, Aspose.Diagram ile önceden ayarlanmış bir temanın bir sayfaya veya şekle nasıl uygulanacağı açıklanmaktadır.
---
## **Bir Sayfaya veya Şekle Hazır Ayar Teması Nasıl Uygulanır?**
Bu makale, VSDX dosyasının temasını Aspose.Diagram kullanarak değiştirmek isteyen herkes için yararlı olabilir. Themes1.vsdx test dosyasını kullanıyoruz, aşağıdakine benzer.

|**Tema1.vsdx**|
|:- |
|![Tema1.vsdx](theme1.png)|

### **Bir Sayfaya Hazır Tema Uygulama**
Aspose.Diagram API'ler, bir sayfada ve birden çok belgede şekillere tekdüze bir görünüm ve his elde etmek için önceden ayarlanmış bir temanın uygulanmasına olanak tanır. Bunu yapmak için aşağıdaki adımları gerçekleştirin:

- diagram yüklemek için Diagram sınıfının bir örneğini oluşturun
- Temayı ayarlamak için bir Sayfa sınıfı örneği alın
- Sayfa örneğinin PresetTheme özelliğine bir Preset değeri atayın
#### **Bir Sayfa Programlama Örneğine Önceden Ayarlanmış Bir Tema Uygulama**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioThemes();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Page class to be set theme
Page page = diagram.Pages[0];
//Assign a Preset value to the PresetTheme property of the Page instance
page.PresetTheme = PresetThemeValue.Bubble;
// Save diagram
diagram.Save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

|**Bir Sayfaya Hazır Tema Uygulamanın Sonucu**|
|:- |
|![SetTheme_out.vsdx](theme2.png)|

### **Bir Sayfaya Önceden Ayarlanmış Tema Varyantı Uygulama**

Aspose.Diagram API'ler, bir sayfada ve birden çok belgede şekillere tekdüze bir görünüm ve his elde etmek için önceden ayarlanmış bir tema varyantının uygulanmasına olanak tanır. Bunu yapmak için aşağıdaki adımları gerçekleştirin:

- diagram yüklemek için Diagram sınıfının bir örneğini oluşturun
- Temayı ayarlamak için bir Sayfa sınıfı örneği alın
- Sayfa örneğinin PresetTheme özelliğine bir Preset değeri atayın
- Sayfa örneğinin PresetThemeVariant özelliğine bir Preset değeri atayın

#### **Bir Sayfa Programlama Örneğine Önceden Ayarlanmış Bir Tema Varyantı Uygulayın**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioThemes();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Page class to be set theme
Page page = diagram.Pages[0];
//Assign a Preset value to the PresetTheme property of the Page instance
page.PresetTheme = PresetThemeValue.Bubble;
//Assign a Preset value to the PresetThemeVariant property of the Page instance
page.PresetThemeVariant = PresetThemeVariantValue.Variant3;
// Save diagram
diagram.Save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}
```

|**Bir Sayfaya Önceden Ayarlanmış Bir Tema Varyantı Uygulamanın Sonucu**|
|:- |
|![SetTheme_out.vsdx](theme3.png)|

### **Bir Şekle Hazır Ayar Teması Uygulama**

Aspose.Diagram API'ler, bir sayfadaki bir şekle önceden ayarlanmış bir temanın uygulanmasına izin verir. Bunu yapmak için aşağıdaki adımları gerçekleştirin:

- diagram yüklemek için Diagram sınıfının bir örneğini oluşturun
- Temayı ayarlamak için Shape sınıfının bir örneğini alın
- Shape örneğinin PresetTheme özelliğine bir Preset değeri atayın

#### **Şekil Programlama Örneğine Hazır Ayar Teması Uygulama**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioThemes();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Shape class to be set theme
Shape shape = doc.Pages[0].Shapes[0];
//Assign a Preset value to the PresetTheme property of the Shape instance
shape.PresetTheme = PresetThemeValue.Bubble;
// Save diagram
diagram.Save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}
```

|**Bir Şekle Hazır Ayar Teması Uygulamanın Sonucu**|
|:- |
|![SetTheme_out.vsdx](theme4.png)|

### **Bir Şekle Hazır Ayar Tema Varyantı Uygulama**

Aspose.Diagram API'ler, bir sayfa içindeki bir şekle önceden ayarlanmış bir tema varyantının uygulanmasına izin verir. Bunu yapmak için aşağıdaki adımları gerçekleştirin:

- diagram yüklemek için Diagram sınıfının bir örneğini oluşturun
- Temayı ayarlamak için Shape sınıfının bir örneğini alın
- Shape örneğinin PresetTheme özelliğine bir Preset değeri atayın
- Shape örneğinin PresetThemeVariant özelliğine bir Preset değeri atayın

#### **Bir Şekil Programlama Örneğine Önceden Ayarlanmış Bir Tema Varyantı Uygulayın**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioThemes();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Shape class to be set theme
Shape shape = doc.Pages[0].Shapes[0];
//Assign a Preset value to the PresetTheme property of the Shape instance
shape.PresetTheme = PresetThemeValue.Bubble;
//Assign a Preset value to the PresetThemeVariant property of the Shape instance
shape.PresetThemeVariant = PresetThemeVariantValue.Variant3;
// Save diagram
diagram.Save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}
```

|**Bir Şekle Hazır Ayar Tema Varyantı Uygulamanın Sonucu**|
|:- |
|![SetTheme_out.vsdx](theme5.png)|

### **Bir Şekle Hazır Ayar Tema Varyantı Hızlı Stili Uygulama**

Aspose.Diagram API'ler, bir sayfa içindeki bir şekle önceden ayarlanmış bir tema hızlı stilinin uygulanmasına izin verir. Bunu yapmak için aşağıdaki adımları gerçekleştirin:

- diagram yüklemek için Diagram sınıfının bir örneğini oluşturun
- Temayı ayarlamak için Shape sınıfının bir örneğini alın
- Shape örneğinin PresetTheme özelliğine bir Preset değeri atayın
- Shape örneğinin PresetThemeVariant özelliğine bir Preset değeri atayın
- Shape örneğinin PresetThemeQuickStyle özelliğine bir Preset değeri atayın

#### **Bir Şekil Programlama Örneğine Hazır Ayar Tema Varyantı Hızlı Stili Uygulama**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioThemes();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Shape class to be set theme
Shape shape = doc.Pages[0].Shapes[0];
//Assign a Preset value to the PresetTheme property of the Shape instance
shape.PresetTheme = PresetThemeValue.Bubble;
//Assign a Preset value to the PresetThemeVariant property of the Shape instance
shape.PresetThemeVariant = PresetThemeVariantValue.Variant3;
//Assign a Preset value to the PresetThemeQuickStyle property of the Shape instance
shape.PresetThemeQuickStyle = PresetQuickStyleValue.VariantStyle2;
// Save diagram
diagram.Save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}
```

|**Bir Şekle Hazır Ayar Tema Varyantı Hızlı Stili Uygulamanın Sonucu**|
|:- |
|![SetTheme_out.vsdx](theme6.png)|

### **SetPresetThemeStyleMatrics Yöntemini Kullanarak Bir Şekle Ön Ayarlı Tema Stili Uygulama**

Aspose.Diagram API'ler, bir sayfa içindeki bir şekle önceden ayarlanmış bir tema hızlı stilinin uygulanmasına izin verir. Bunu yapmak için aşağıdaki adımları gerçekleştirin:

- diagram yüklemek için Diagram sınıfının bir örneğini oluşturun
- Temayı ayarlamak için Shape sınıfının bir örneğini alın
- Shape örneğinin PresetTheme özelliğine bir Preset değeri atayın
- Shape örneğinin PresetThemeVariant özelliğine bir Preset değeri atayın
- SetPresetThemeStyleMatrics Yöntemini kullanarak Shape örneğinin stil değerini ve renk değerini ayarlayarak bir tema stili atayın

#### **SetPresetThemeStyleMatrics Yöntemi Programlama Örneği Kullanarak Bir Şekle Ön Ayarlı Tema Stili Uygulama**

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioThemes();
// Load diagram
Diagram diagram = new Diagram(dataDir + "Themes1.vsdx");
//Get an instance of Shape class to be set theme
Shape shape = doc.Pages[0].Shapes[0];
//Assign a Preset value to the PresetTheme property of the Shape instance
shape.PresetTheme = PresetThemeValue.Bubble;
//Assign a Preset value to the PresetThemeVariant property of the Shape instance
shape.PresetThemeVariant = PresetThemeVariantValue.Variant3;
//Assign a theme style by setting style value and color value of the Shape instance
shape.SetPresetThemeStyleMatrics(PresetStyleMatricsValue.Style2, PresetColorMatricsValue.Color7);
// Save diagram
diagram.Save(dataDir + "SetTheme_out.vsdx", SaveFileFormat.VSDX);
{{< /highlight >}}
```

|**SetPresetThemeStyleMatrics Yöntemini Kullanarak Bir Şekle Ön Ayarlı Tema Stili Uygulamanın Sonucu**|
|:- |
|![SetTheme_out.vsdx](theme7.png)|
