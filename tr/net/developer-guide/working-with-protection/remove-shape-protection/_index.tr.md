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

```
{{< highlight "csharp" >}}
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
shape.Protection.LockAspect.Value = BOOL.False;
shape.Protection.LockBegin.Value = BOOL.False;
shape.Protection.LockCalcWH.Value = BOOL.False;
shape.Protection.LockCrop.Value = BOOL.False;
shape.Protection.LockCustProp.Value = BOOL.False;
shape.Protection.LockDelete.Value = BOOL.False;
shape.Protection.LockEnd.Value = BOOL.False;
shape.Protection.LockFormat.Value = BOOL.False;
shape.Protection.LockFromGroupFormat.Value = BOOL.False;
shape.Protection.LockGroup.Value = BOOL.False;
shape.Protection.LockHeight.Value = BOOL.False;
shape.Protection.LockMoveX.Value = BOOL.False;
shape.Protection.LockMoveY.Value = BOOL.False;
shape.Protection.LockRotate.Value = BOOL.False;
shape.Protection.LockSelect.Value = BOOL.False;
shape.Protection.LockTextEdit.Value = BOOL.False;
shape.Protection.LockThemeColors.Value = BOOL.False;
shape.Protection.LockThemeEffects.Value = BOOL.False;
shape.Protection.LockVtxEdit.Value = BOOL.False;
shape.Protection.LockWidth.Value = BOOL.False;
            
// Save diagram
diagram.Save(dataDir + "RemoveShapeProtection_out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
