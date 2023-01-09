---
title: Koruma ile Çalışma
type: docs
weight: 170
url: /tr/net/working-with-protection/
description: Bu bölüm, diagram'de Aspose.Diagram ile korumanın nasıl ayarlanacağını açıklar.
---
## **Visio Diagram Set Koruması**
 Diyagramları korumak, kullanıcıların arka planları, kalıpları (kalıpları), şekilleri ve stilleri düzenlenemeyecek şekilde kilitlemesine olanak tanır. Bu, örneğin kurumsal stilleri korumak ve bir dizi diyagramda tutarlı bir görünüm sağlamak için kullanışlıdır. Geliştiriciler bunu kullanarak başarabilir[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Visio Diagram Korumasını düzenleyin**
tarafından sunulan ProtectBkgnds, ProtectMasters, ProtectShapes ve ProtectStyles özellikleri[Belge Ayarları](http://www.aspose.com/api/net/diagram/aspose.diagram/documentsettings) sınıfı, Aspose.Diagram.BoolValue nesnesini destekler. Bu özellikler Microsoft Office Visio diyagramlarını korumak ve korumayı kaldırmak için kullanılabilir. Microsoft Visio'de belgeleri şu şekilde korursunuz:

1. Microsoft Visio'de bir diagram açın.
1. Çizim Gezgini penceresini açın.
1.  Bir diagram'e sağ tıklayın ve seçin**Belgeyi Koru** menüden.
1. Belgeyi Koru penceresinde, farklı diagram öğelerini kilitlemek veya kilidini açmak için seçenekleri işaretleyin veya temizleyin.
1.  Tıklamak**TAMAM**.
#### **Diagram Koruma Programlama Örneği'ni düzenleyin**
Aspose.Diagram for .NET API kullanarak Visio diagram'in farklı öğelerini kilitlemek ve kilidini açmak gibi aynı görevleri gerçekleştirmek için aşağıdaki kodu bir .NET uygulamasında kullanın.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Protection-VisioDiagramProtection-VisioDiagramProtection.cs" >}}
## **Visio Şeklinin Set Koruması**
 Visio şekillerinin korunması, kullanıcıların şekillerin belirli yönlerini kilitlemesine olanak tanır. Şekil koruması yoluyla kilitlenebilen şekillerin özellikleri arasında genişlik, yükseklik, x konumu, y konumu, döndürme ve daha fazlası bulunur. Geliştiriciler bunu kullanarak başarabilir[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Visio Şekil Korumasını düzenleyin**
**KilitAspect**, **Kilitle Başla**, **LockCalcWH**, **Kilit Kırpma**, **LockCustProp**, **KilitleSil**, **KilitSonu**, **Kilit Biçimi**, **LockFromGroupFormat**, **Kilit Grubu**, **Kilit Yüksekliği**, **KilitMoveX**, **LockMoveY**, **KilitleDöndür**, **Seçimi Kilitle**, **LockTextDüzenle**, **LockThemeColors**, **LockThemeEffects**, **LockVtxDüzenle** ve**Kilit Genişliği** maruz kalan özellikler[**Koruma**](http://www.aspose.com/api/net/diagram/aspose.diagram/Protection) sınıf desteği**Aspose.Diagram.BoolValue** nesne. Bu özellikler, şekilleri korumak ve korumayı kaldırmak için kullanılabilir.

Microsoft Office Visio'de kullanıcı herhangi bir şekli korumak için aşağıdaki işlemleri yapabilir:

- Açık diagram içinde Microsoft Office Visio
- Herhangi bir şekli seçin
- Visio 2007 kullanıyorsanız 'Format' menüsünden 'Koruma…' seçeneğini veya Visio 2010 kullanıyorsanız 'Geliştirici' menüsünden 'Koruma'yı seçin.
- Herhangi bir şekil özelliğini kilitlemek veya kilidini açmak için "Koruma" penceresinde herhangi bir metin kutusunu işaretleyin/işaretini kaldırın
- Tamam tuşuna basın'
### **Şekil Koruma Programlama Örneğinin Düzenlenmesi**
Aspose.Diagram for .NET kullanarak aynı şeyi yapmak (herhangi bir şekil özniteliğini kilitlemek/kilidini açmak) için .NET uygulamanızda aşağıdaki kodu kullanın.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Protection-VisioShapeProtection-VisioShapeProtection.cs" >}}
