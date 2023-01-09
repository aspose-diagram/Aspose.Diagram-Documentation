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
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Theme-SetThemeForPage.cs" >}}

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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Theme-SetThemeVariantForPage.cs" >}}

|**Bir Sayfaya Önceden Ayarlanmış Bir Tema Varyantı Uygulamanın Sonucu**|
|:- |
|![SetTheme_out.vsdx](theme3.png)|

### **Bir Şekle Hazır Ayar Teması Uygulama**

Aspose.Diagram API'ler, bir sayfadaki bir şekle önceden ayarlanmış bir temanın uygulanmasına izin verir. Bunu yapmak için aşağıdaki adımları gerçekleştirin:

- diagram yüklemek için Diagram sınıfının bir örneğini oluşturun
- Temayı ayarlamak için Shape sınıfının bir örneğini alın
- Shape örneğinin PresetTheme özelliğine bir Preset değeri atayın

#### **Şekil Programlama Örneğine Hazır Ayar Teması Uygulama**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Theme-SetThemeForShape.cs" >}}

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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Theme-SetThemeVariantForShape.cs" >}}

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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Theme-SetThemeQuickStyleForShape.cs" >}}

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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Theme-SetThemeStyleMatricsForShape.cs" >}}

|**SetPresetThemeStyleMatrics Yöntemini Kullanarak Bir Şekle Ön Ayarlı Tema Stili Uygulamanın Sonucu**|
|:- |
|![SetTheme_out.vsdx](theme7.png)|
