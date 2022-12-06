---
title: Koruma ile Çalışma
type: docs
weight: 90
url: /tr/python-java/working-with-protection/
---
## **Visio Diagram Set Koruması**
Diyagramları korumak, kullanıcıların arka planları, kalıpları (kalıpları), şekilleri ve stilleri düzenlenemeyecek şekilde kilitlemesine olanak tanır. Bu, örneğin kurumsal stilleri korumak ve bir dizi diyagramda tutarlı bir görünüm sağlamak için kullanışlıdır. Geliştiriciler, Java aracılığıyla Python için Aspose.Diagram'i kullanarak bunu başarabilir.

### **Visio Diagram'in Korumasını Düzenle**
DocumentSettings sınıfı tarafından sunulan getProtectBkgnds, getProtectMasters, getProtectShapes ve getProtectStyles yöntemleri BoolValue nesnesini destekler. Bu özellikler Microsoft Visio diyagramlarını korumak ve korumayı kaldırmak için kullanılabilir.

Microsoft Visio'de belgeleri şu şekilde korursunuz:

1. Microsoft Visio'de bir diagram açın.
1. Çizim Gezgini penceresini açın.
1.  Bir diagram'e sağ tıklayın ve seçin**Belgeyi Koru** menüden.
1. Belgeyi Koru penceresinde, farklı diagram öğelerini kilitlemek veya kilidini açmak için seçenekleri işaretleyin veya temizleyin.
1.  Tıklamak**TAMAM**.

**Lütfen seçenekleri manuel olarak nasıl kontrol edebileceğimizi veya temizleyebileceğimizi görün.** 

diagram üzerinden Python için Aspose.Diagram'i kullanarak aynı görevleri gerçekleştirmek için uygulamanızda aşağıdaki kodu kullanın - diagram'inizin farklı öğelerini kilitleyin ve kilidini açın.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-VisioDiagramProtection.py" >}}

### **Visio Şekil Korumasını düzenleyin**
Visio şekillerinin korunması, kullanıcıların şekillerin belirli yönlerini kilitlemesine olanak tanır. Şekil koruması yoluyla kilitlenebilen şekillerin özellikleri arasında genişlik, yükseklik, x konumu, y konumu, döndürme ve daha fazlası bulunur. Geliştiriciler, Java aracılığıyla Python için Aspose.Diagram'i kullanarak bunu başarabilir.

 bu**getLockAspect()**, **getLockBegin()**, **getLockCalcWH()**, **getLockCrop()**, **getLockCustProp()**, **getLockDelete()**, **getLockEnd()**, **getLockFormat()**, **getLockFromGroupFormat()**, **getLockGroup()**, **getLockHeight()**, **getLockMoveX()**, **getLockMoveY()**, **getLockRotate()**, **getLockSelect()**, **getLockTextEdit()**, **getLockThemeColors()**, **getLockThemeEffects()**, **getLockVtxEdit()** ve**getLockWidth()** maruz kalan yöntemler**Koruma** sınıf, BoolValue nesnesini destekler. Bu yöntemler şekilleri korumak/korumayı kaldırmak için kullanılabilir.

Visio'de, herhangi bir şekli korumak için aşağıdaki işlemleri yapmanız gerekir:

1. Microsoft Visio'de bir diagram açın.
1. Bir şekil seçin.
1.  Seçme**Koruma** dan**Biçim** menüsü (Visio 2007) veya**Koruma** dan**Geliştirici** menü (Visio 2010).
1.  İçinde**Koruma** penceresinde, şekil niteliğini kilitlemek veya kilidini açmak için seçenekleri seçin veya temizleyin.
1.  Tıklamak**TAMAM**.

**Microsoft Visio'de görüldüğü gibi bir şeklin koruma seçenekleri** 

Java ile Python için Aspose.Diagram'i kullanarak aynı şeyi yapmak (herhangi bir şekil özniteliğini kilitlemek/kilidini açmak) için Java uygulamanızda aşağıdaki kodu kullanın.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-VisioShapeProtection.py" >}}
