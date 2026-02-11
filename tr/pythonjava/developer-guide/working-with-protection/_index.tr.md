---
title: Koruma ile Çalışma
type: docs
weight: 90
url: /tr/python-java/working-with-protection/
---
## **Visio Diagram Set Koruması**
Diyagramları korumak, kullanıcıların arka planları, kalıpları (kalıpları), şekilleri ve stilleri düzenlenemeyecek şekilde kilitlemesine olanak tanır. Bu, örneğin kurumsal stilleri korumak ve bir dizi diyagramda tutarlı bir görünüm sağlamak için kullanışlıdır. Geliştiriciler, Python via Java için Aspose.Diagram'i kullanarak bunu başarabilir.

### **Visio Diagram'in Korumasını Düzenle**
DocumentSettings sınıfı tarafından sunulan getProtectBkgnds, getProtectMasters, getProtectShapes ve getProtectStyles yöntemleri BoolValue nesnesini destekler. Bu özellikler Microsoft Visio diyagramlarını korumak ve korumayı kaldırmak için kullanılabilir.

Microsoft Visio'de belgeleri şu şekilde korursunuz:

1. Microsoft Visio'de bir diagram açın.
1. Çizim Gezgini penceresini açın.
1.  Bir diagram'e sağ tıklayın ve seçin**Belgeyi Koru** menüden.
1. Belgeyi Koru penceresinde, farklı diagram öğelerini kilitlemek veya kilidini açmak için seçenekleri işaretleyin veya temizleyin.
1.  Tıklamak**TAMAM**.

**Lütfen seçenekleri manuel olarak nasıl kontrol edebileceğimizi veya temizleyebileceğimizi görün.** 

Python via Java için Aspose.Diagram'i kullanarak aynı görevleri gerçekleştirmek için uygulamanızda aşağıdaki kodu kullanın - diagram'inizin farklı öğelerini kilitleyin ve kilidini açın.


{{< highlight python >}}
import jpype
import asposediagram
jpype.startJVM()
from asposediagram.api import *

lic = License()
lic.setLicense("Aspose.Total.Product.Family.lic")

# Load diagram
diagram = Diagram("ProtectAndUnprotect.vsd")

diagram.getDocumentSettings().setProtectBkgnds(BOOL.TRUE)
diagram.getDocumentSettings().setProtectMasters(BOOL.TRUE)
diagram.getDocumentSettings().setProtectShapes(BOOL.TRUE)
diagram.getDocumentSettings().setProtectStyles(BOOL.TRUE)

# save diagram
diagram.save("VisioDiagramProtection_Out.vsdx", SaveFileFormat.VSDX)

jpype.shutdownJVM()

{{< /highlight >}}


### **Visio Şekil Korumasını düzenleyin**
Visio şekillerinin korunması, kullanıcıların şekillerin belirli yönlerini kilitlemesine olanak tanır. Şekil koruması yoluyla kilitlenebilen şekillerin özellikleri arasında genişlik, yükseklik, x konumu, y konumu, döndürme ve daha fazlası bulunur. Geliştiriciler, Python via Java için Aspose.Diagram'i kullanarak bunu başarabilir.

 bu**getLockAspect()**, **getLockBegin()**, **getLockCalcWH()**, **getLockCrop()**, **getLockCustProp()**, **getLockDelete()**, **getLockEnd()**, **getLockFormat()**, **getLockFromGroupFormat()**, **getLockGroup()**, **getLockHeight()**, **getLockMoveX()**, **getLockMoveY()**, **getLockRotate()**, **getLockSelect()**, **getLockTextEdit()**, **getLockThemeColors()**, **getLockThemeEffects()**, **getLockVtxEdit()** ve**getLockWidth()** maruz kalan yöntemler**Koruma** sınıf, BoolValue nesnesini destekler. Bu yöntemler şekilleri korumak/korumayı kaldırmak için kullanılabilir.

Visio'de, herhangi bir şekli korumak için aşağıdaki işlemleri yapmanız gerekir:

1. Microsoft Visio'de bir diagram açın.
1. Bir şekil seçin.
1.  Seçme**Koruma** dan**Biçim** menüsü (Visio 2007) veya**Koruma** dan**Geliştirici** menü (Visio 2010).
1.  İçinde**Koruma** penceresinde, şekil niteliğini kilitlemek veya kilidini açmak için seçenekleri seçin veya temizleyin.
1.  Tıklamak**TAMAM**.

**Microsoft Visio'de görüldüğü gibi bir şeklin koruma seçenekleri** 

Python via Java için Aspose.Diagram'i kullanarak aynı şeyi yapmak (herhangi bir şekil özniteliğini kilitlemek/kilidini açmak) için Java uygulamanızda aşağıdaki kodu kullanın.


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
shape.getProtection().getLockAspect().setValue(BOOL.TRUE)
shape.getProtection().getLockBegin().setValue(BOOL.TRUE)
shape.getProtection().getLockCalcWH().setValue(BOOL.TRUE)
shape.getProtection().getLockCrop().setValue(BOOL.TRUE)
shape.getProtection().getLockCustProp().setValue(BOOL.TRUE)
shape.getProtection().getLockDelete().setValue(BOOL.TRUE)
shape.getProtection().getLockEnd().setValue(BOOL.TRUE)
shape.getProtection().getLockFormat().setValue(BOOL.TRUE)
shape.getProtection().getLockFromGroupFormat().setValue(BOOL.TRUE)
shape.getProtection().getLockGroup().setValue(BOOL.TRUE)
shape.getProtection().getLockHeight().setValue(BOOL.TRUE)
shape.getProtection().getLockMoveX().setValue(BOOL.TRUE)
shape.getProtection().getLockMoveY().setValue(BOOL.TRUE)
shape.getProtection().getLockRotate().setValue(BOOL.TRUE)
shape.getProtection().getLockSelect().setValue(BOOL.TRUE)
shape.getProtection().getLockTextEdit().setValue(BOOL.TRUE)
shape.getProtection().getLockThemeColors().setValue(BOOL.TRUE)
shape.getProtection().getLockThemeEffects().setValue(BOOL.TRUE)
shape.getProtection().getLockVtxEdit().setValue(BOOL.TRUE)
shape.getProtection().getLockWidth().setValue(BOOL.TRUE)
        
# save diagram
diagram.save("VisioShapeProtection_Out.vdx", SaveFileFormat.VDX)
jpype.shutdownJVM()

{{< /highlight >}}

