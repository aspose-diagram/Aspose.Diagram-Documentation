---
title: Şekil Korumasını Kaldır
type: docs
weight: 20
url: /tr/python-java/remove-shape-protection/
description: Bu bölümde, Java aracılığıyla Python için Aspose.Diagram kullanılarak şekil korumasının nasıl kaldırılacağı açıklanmaktadır.
---
## **Visio Şeklinin Korumasını Kaldırma**
Visio şekillerinin korunması, kullanıcıların şekillerin belirli yönlerini kilitlemesine olanak tanır. Şekil koruması yoluyla kilitlenebilen şekillerin özellikleri arasında genişlik, yükseklik, x konumu, y konumu, döndürme ve daha fazlası bulunur. Geliştiriciler, Java aracılığıyla Python için Aspose.Diagram'i kullanarak bunu başarabilir.
### **Visio Şekil Korumasını düzenleyin**
**KilitAspect**, **Kilitle Başla**, **LockCalcWH**, **Kilit Kırpma**, **LockCustProp**, **KilitleSil**, **KilitSonu**, **Kilit Biçimi**, **LockFromGroupFormat**, **Kilit Grubu**, **Kilit Yüksekliği**, **KilitMoveX**, **LockMoveY**, **KilitleDöndür**, **Seçimi Kilitle**, **LockTextDüzenle**, **LockThemeColors**, **LockThemeEffects**, **LockVtxDüzenle** ve**Kilit Genişliği** maruz kalan özellikler**Koruma** sınıf desteği**Aspose.Diagram.BoolValue** nesne. Bu özellikler, şekilleri korumak ve korumayı kaldırmak için kullanılabilir.

Microsoft Office Visio'de kullanıcı herhangi bir şekli korumak için aşağıdaki işlemleri yapabilir:

- Açık diagram içinde Microsoft Office Visio
- Herhangi bir şekli seçin
- Visio 2007 kullanıyorsanız 'Format' menüsünden 'Koruma'yı, Visio 2010 kullanıyorsanız 'Geliştirici' menüsünden 'Koruma'yı seçin
- Herhangi bir şekil özelliğinin kilidini açmak için "Koruma" penceresinde herhangi bir metin kutusunun işaretini kaldırın.
- Tamam tuşuna basın'

### **Şekil Koruma Programlama Örneğinin Kaldırılması**
Python üzerinden Java için Aspose.Diagram'i kullanarak aynı şeyi yapmak (herhangi bir şekil özniteliğinin kilidini açmak) için uygulamanızda aşağıdaki kodu kullanın.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-RemoveShapeProtection.py" >}}

