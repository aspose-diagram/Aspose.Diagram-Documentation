---
title: Şekil Korumasını Kaldır
type: docs
weight: 20
url: /tr/python-java/remove-shape-protection/
description: Bu bölümde, Python via Java için Aspose.Diagram kullanılarak şekil korumasının nasıl kaldırılacağı açıklanmaktadır.
---
## **Visio Şeklinin Korumasını Kaldırma**
Visio şekillerinin korunması, kullanıcıların şekillerin belirli yönlerini kilitlemesine olanak tanır. Şekil koruması yoluyla kilitlenebilen şekillerin özellikleri arasında genişlik, yükseklik, x konumu, y konumu, döndürme ve daha fazlası bulunur. Geliştiriciler, Python via Java için Aspose.Diagram'i kullanarak bunu başarabilir.
### **Visio Şekil Korumasını düzenleyin**
**KilitAspect**, **Kilitle Başla**, **LockCalcWH**, **Kilit Kırpma**, **LockCustProp**, **KilitleSil**, **KilitSonu**, **Kilit Biçimi**, **LockFromGroupFormat**, **Kilit Grubu**, **Kilit Yüksekliği**, **KilitMoveX**, **LockMoveY**, **KilitleDöndür**, **Seçimi Kilitle**, **LockTextDüzenle**, **LockThemeColors**, **LockThemeEffects**, **LockVtxDüzenle** ve**Kilit Genişliği** maruz kalan özellikler**Koruma** sınıf desteği**Aspose.Diagram.BoolValue** nesne. Bu özellikler, şekilleri korumak ve korumayı kaldırmak için kullanılabilir.

Microsoft Office Visio'de kullanıcı herhangi bir şekli korumak için aşağıdaki işlemleri yapabilir:

- Açık diagram içinde Microsoft Office Visio
- Herhangi bir şekli seçin
- Visio 2007 kullanıyorsanız 'Format' menüsünden 'Koruma'yı, Visio 2010 kullanıyorsanız 'Geliştirici' menüsünden 'Koruma'yı seçin
- Herhangi bir şekil özelliğinin kilidini açmak için "Koruma" penceresinde herhangi bir metin kutusunun işaretini kaldırın.
- Tamam tuşuna basın'

### **Şekil Koruma Programlama Örneğinin Kaldırılması**
Python via Java için Aspose.Diagram'i kullanarak aynı şeyi yapmak (herhangi bir şekil özniteliğinin kilidini açmak) için uygulamanızda aşağıdaki kodu kullanın.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Load diagram
diagram = Diagram("ProtectAndUnprotect.vsd")
# get page by name
page = diagram.getPages().getPage("Flow 1")
# get shape by ID
shape = page.getShapes().getShape(1)

# set protections
shape.getProtection().getLockAspect().setValue(BOOL.FALSE)
shape.getProtection().getLockBegin().setValue(BOOL.FALSE)
shape.getProtection().getLockCalcWH().setValue(BOOL.FALSE)
shape.getProtection().getLockCrop().setValue(BOOL.FALSE)
shape.getProtection().getLockCustProp().setValue(BOOL.FALSE)
shape.getProtection().getLockDelete().setValue(BOOL.FALSE)
shape.getProtection().getLockEnd().setValue(BOOL.FALSE)
shape.getProtection().getLockFormat().setValue(BOOL.FALSE)
shape.getProtection().getLockFromGroupFormat().setValue(BOOL.FALSE)
shape.getProtection().getLockGroup().setValue(BOOL.FALSE)
shape.getProtection().getLockHeight().setValue(BOOL.FALSE)
shape.getProtection().getLockMoveX().setValue(BOOL.FALSE)
shape.getProtection().getLockMoveY().setValue(BOOL.FALSE)
shape.getProtection().getLockRotate().setValue(BOOL.FALSE)
shape.getProtection().getLockSelect().setValue(BOOL.FALSE)
shape.getProtection().getLockTextEdit().setValue(BOOL.FALSE)
shape.getProtection().getLockThemeColors().setValue(BOOL.FALSE)
shape.getProtection().getLockThemeEffects().setValue(BOOL.FALSE)
shape.getProtection().getLockVtxEdit().setValue(BOOL.FALSE)
shape.getProtection().getLockWidth().setValue(BOOL.FALSE)
        
# save diagram
diagram.save("VisioShapeProtection_Out.vsdx", SaveFileFormat.VSDX)
jpype.shutdownJVM()

{{< /highlight >}}


