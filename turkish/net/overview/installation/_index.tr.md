---
title: Kurulum
type: docs
weight: 40
url: /tr/net/installation/
description: Bu sayfada, Aspose.Diagram kitaplığıyla yeni visio'in nasıl oluşturulacağı açıklanmaktadır.
---
## **Kurulum Aspose.Diagram for .NET - NuGet**
NuGet, geliştirme sırasında üçüncü taraf kitaplıklarını bir .NET uygulamasına dahil etme sürecini basitleştirmeyi amaçlayan, .NET platformu için ücretsiz, açık kaynaklı, geliştirici odaklı bir paket yönetim sistemidir. .NET Framework kullanan Visual Studio projelerinde kitaplıkların ve araçların eklenmesini, kaldırılmasını ve güncellenmesini kolaylaştıran bir Visual Studio uzantısıdır. Bir kitaplık veya araç, NuGet paketi oluşturularak ve içinde saklanarak diğer geliştiricilerle kolayca paylaşılabilir bir NuGet deposu. Paketi kurduğunuzda, NuGet dosyaları çözümünüze kopyalar ve referans ekleme ve app.config veya web.config dosyalarınızı değiştirme gibi gerekli değişiklikleri otomatik olarak yapar. Kitaplığı kaldırmaya karar verirseniz, NuGet dosyaları kaldırır ve projenizde yaptığı değişiklikleri geri alır, böylece hiçbir karmaşa kalmaz.
### **Referans Aspose.Diagram for .NET**
Bu harika özellikten yararlanarak,[Aspose.Diagram for .NET](https://www.nuget.org/packages/Aspose.Diagram)kitaplıkları bir NuGet paketine ve bir NuGet deposuna yükledi. Bu seçenek ile sisteminize bu bileşeni kurmadan Aspose.Diagram for .NET kullanma avantajına sahip olursunuz. NuGet, Visual Studio 2010 ve üzeri sürüm(ler), Visual Web Developer 2010 ve Windows Phone Developer Tools 7.1'de çalışır. Testlerimizde Visual Studio 2015 Ultimate ile test ettik.

Başlamak:

1. Çözümünüzü veya projenizi Visual Studio'da açın.
1. NuGet Paket Yöneticisi'ni Visual Studio uzantısı olarak ekleyin:
 1.**Aletler**menü ardından**Uzantı Yöneticisi**.
 1. Seçin**Çevrimiçi Galeri**çevrimiçi olarak sunulan paketlerin tam bir listesini almak için.
 1. Seçin**NuGet Paket Yöneticisi**.
 1. tıklayın**İndirmek**.
 1. Paket Yöneticisi yüklendikten sonra, değişiklikleri etkinleştirmek için Visual Studio'yu yeniden başlatın.
NuGet Paket Yöneticisi kurulduğunda, paketleri bulabilir, kurabilir, kaldırabilir ve güncelleyebilirsiniz.**NuGet Paketlerini Yönet**penceresinde veya PowerShell komut satırı komutlarını kullanarak**Paket Yöneticisi Konsolu**özel Visual Studio penceresi. öğesini seçerseniz her iki seçeneği de bulabilirsiniz.**Aletler**bunu takiben**Kitaplık Paket Yöneticisi**.
### **Paket Yöneticisi Konsolunu Kullanarak Paketi Kurun**
Paket yöneticisi konsolunu kullanarak bileşene başvurmak için:

1. .NET uygulamanızı Visual Studio'da açın.
1. Üzerinde**Aletler**menü, seç**Kitaplık Paket Yöneticisi**ve daha sonra**Paket Yöneticisi Konsolu**.
1. En son tam sürümü yüklemek için "Install-Package Aspose.Diagram" komutunu yazın veya düzeltmeler dahil en son sürümü yüklemek için "Install-Package Aspose.Diagram -prerelease" komutunu yazın.
1. Basmak**Girmek**.
### **Paket Yöneticisi Konsolunu kullanarak paketi güncelleyin**
Bileşene zaten NuGet aracılığıyla başvurduysanız, referansı en son sürüme güncellemek için şu adımları izleyin:

1. .NET numaralı uygulamayı Visual Studio'da açın.
1. itibaren**Aletler**menü, seç**Kitaplık Paket Yöneticisi**, bunu takiben**Paket Yöneticisi Konsolu**Paket Yöneticisi konsolunu açmak için.
1. En son tam sürüme başvurmak için "Update-Package Aspose.Diagram" komutunu yazın veya düzeltmeler dahil en son sürümü yüklemek için "Update-Package Aspose.Diagram -prerelease" komutunu yazın.
1. Basmak**Girmek**.
### **Paket Yöneticisi GUI'sini kullanarak Paketi Kurun**
Paket yöneticisi GUI'sini kullanarak bileşene başvurmak için şu adımları izleyin:

1. .NET numaralı uygulamayı Visual Studio'da açın.
1. itibaren**Aletler**menü, seç**Kitaplık Paket Yöneticisi**ve**NuGet Paketlerini Yönet**dan**Çözüm**seçenek.
 Çözüm Gezgini'nden de benzer bir seçenek alabilirsiniz:
 1. Proje adına sağ tıklayın.
 1. Seçin**NuGet Paketlerini Yönet**.
1. Seçme**internet üzerinden**sol menüden
1. Tip**Aspose.Diagram**Aspose.Diagram for .NET'i bulmak için arama kutusuna girin.
1. Tıklamak**Güncellemeyi yükle**en son sürümün yanında Aspose.Diagram for .NET

**![Aspose Diagram ila NuGet'i yükleyin](nuget.png aracılığıyla yükleyin)**
