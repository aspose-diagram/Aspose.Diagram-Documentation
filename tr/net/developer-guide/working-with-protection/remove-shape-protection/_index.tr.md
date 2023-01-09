---
title: Şekil Korumasını Kaldır
type: docs
weight: 20
url: /tr/net/remove-shape-protection/
description: Bu bölümde şekil korumasının nasıl kaldırılacağı açıklanmaktadır.
---
## **Visio Şeklinin Korumasını Kaldırma**
 Visio şekillerinin korunması, kullanıcıların şekillerin belirli yönlerini kilitlemesine olanak tanır. Şekil koruması yoluyla kilitlenebilen şekillerin özellikleri arasında genişlik, yükseklik, x konumu, y konumu, döndürme ve daha fazlası bulunur. Geliştiriciler bunu kullanarak başarabilir[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).
### **Visio Şekil Korumasını düzenleyin**
**KilitAspect**, **Kilitle Başla**, **LockCalcWH**, **Kilit Kırpma**, **LockCustProp**, **KilitleSil**, **KilitSonu**, **Kilit Biçimi**, **LockFromGroupFormat**, **Kilit Grubu**, **Kilit Yüksekliği**, **KilitMoveX**, **LockMoveY**, **KilitleDöndür**, **Seçimi Kilitle**, **LockTextDüzenle**, **LockThemeColors**, **LockThemeEffects**, **LockVtxDüzenle** ve**Kilit Genişliği** maruz kalan özellikler[**Koruma**](http://www.aspose.com/api/net/diagram/aspose.diagram/Protection) sınıf desteği**Aspose.Diagram.BoolValue** nesne. Bu özellikler, şekilleri korumak ve korumayı kaldırmak için kullanılabilir.

Microsoft Office Visio'de kullanıcı herhangi bir şekli korumak için aşağıdaki işlemleri yapabilir:

- Açık diagram içinde Microsoft Office Visio
- Herhangi bir şekli seçin
- Visio 2007 kullanıyorsanız 'Format' menüsünden 'Koruma'yı, Visio 2010 kullanıyorsanız 'Geliştirici' menüsünden 'Koruma'yı seçin
- Herhangi bir şekil özelliğinin kilidini açmak için "Koruma" penceresinde herhangi bir metin kutusunun işaretini kaldırın.
- Tamam tuşuna basın'
### **Şekil Koruma Programlama Örneğinin Kaldırılması**
Aspose.Diagram for .NET kullanarak aynı şeyi yapmak (herhangi bir şekil özniteliğinin kilidini açmak) için .NET uygulamanızda aşağıdaki kodu kullanın.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-with-Protection-RemoveShapeProtection-RemoveShapeProtection.cs" >}}
