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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Protection();

// Load diagram
Diagram diagram = new Diagram(dataDir + "ProtectAndUnprotect.vsd");

diagram.DocumentSettings.ProtectBkgnds = BOOL.True;
diagram.DocumentSettings.ProtectMasters = BOOL.True;
diagram.DocumentSettings.ProtectShapes = BOOL.True;
diagram.DocumentSettings.ProtectStyles = BOOL.True;
// Save diagram
diagram.Save(dataDir + "VisioDiagramProtection_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

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


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Protection();

// Load diagram
Diagram diagram = new Diagram(dataDir + "ProtectAndUnprotect.vsd");
// Get page by name
Page page = diagram.Pages.GetPage("Flow 1");
// Get shape by ID
Shape shape = page.Shapes.GetShape(1);

// Set protections
shape.Protection.LockAspect.Value = BOOL.True;
shape.Protection.LockBegin.Value = BOOL.True;
shape.Protection.LockCalcWH.Value = BOOL.True;
shape.Protection.LockCrop.Value = BOOL.True;
shape.Protection.LockCustProp.Value = BOOL.True;
shape.Protection.LockDelete.Value = BOOL.True;
shape.Protection.LockEnd.Value = BOOL.True;
shape.Protection.LockFormat.Value = BOOL.True;
shape.Protection.LockFromGroupFormat.Value = BOOL.True;
shape.Protection.LockGroup.Value = BOOL.True;
shape.Protection.LockHeight.Value = BOOL.True;
shape.Protection.LockMoveX.Value = BOOL.True;
shape.Protection.LockMoveY.Value = BOOL.True;
shape.Protection.LockRotate.Value = BOOL.True;
shape.Protection.LockSelect.Value = BOOL.True;
shape.Protection.LockTextEdit.Value = BOOL.True;
shape.Protection.LockThemeColors.Value = BOOL.True;
shape.Protection.LockThemeEffects.Value = BOOL.True;
shape.Protection.LockVtxEdit.Value = BOOL.True;
shape.Protection.LockWidth.Value = BOOL.True;
            
// Save diagram
diagram.Save(dataDir + "VisioShapeProtection_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

