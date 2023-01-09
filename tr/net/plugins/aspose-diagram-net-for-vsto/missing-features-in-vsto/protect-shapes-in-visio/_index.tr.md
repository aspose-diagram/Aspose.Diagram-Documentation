---
title: Visio'de Şekilleri Koruyun
type: docs
weight: 20
url: /tr/net/protect-shapes-in-visio/
---
Koruma sınıfı tarafından kullanıma sunulan LockAspect, LockBegin, LockCalcWH, LockCrop, LockCustProp, LockDelete, LockEnd, LockFormat, LockFromGroupFormat, LockGroup, LockHeight, LockMoveX, LockMoveY, LockRotate, LockSelect, LockTextEdit, LockThemeColors, LockThemeEffects, LockVtxEdit ve LockWidth özellikleri Aspose.Diagram.BoolValue nesnesini destekler . Bu özellikler, şekilleri korumak/korumayı kaldırmak için kullanılabilir.

Visio'de, herhangi bir şekli korumak için aşağıdaki işlemleri yapmanız gerekir:

- MS Visio'de diagram'i açın
- Herhangi bir şekli seçin
- Visio 2007 kullanıyorsanız 'Format' menüsünden 'Koruma…' seçeneğini veya Visio 2010 kullanıyorsanız 'Geliştirici' menüsünden 'Koruma'yı seçin.
- Herhangi bir şekil özelliğini kilitlemek veya kilidini açmak için "Koruma" penceresinde herhangi bir metin kutusunu işaretleyin/işaretini kaldırın
- Tamam tuşuna basın'

Aspose.Diagram for .NET kullanarak aynı şeyi yapmak (herhangi bir şekil özniteliğini kilitlemek) için .NET uygulamanızda aşağıdaki kodu kullanın.

{{< highlight "csharp" >}}

 //Load diagram

Diagram diagram = new Diagram("ProtectShape.vsd");

Page page0 = diagram.Pages[0];

Shape shape = page0.Shapes[0];

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

diagram.Save("ProtectedShapesFile.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
## **Örnek Kodu İndir**
- [Bitbucket](https://bitbucket.org/asposemarketplace/aspose-for-vsto/src/master/Aspose.Diagram%20Vs%20VSTO%20Visio/)
