---
title: Şekil Korumasını Kaldır
type: docs
weight: 20
url: /tr/java/remove-shape-protection/
description: Bu bölüm, Aspose.Diagram kullanarak şekil korumasının nasıl kaldırılacağını açıklar.
---
## **Visio Şeklinin Korumasını Kaldırma**
 Visio şekillerinin korunması, kullanıcıların şekillerin belirli yönlerini kilitlemesine olanak tanır. Şekil koruması yoluyla kilitlenebilen şekillerin özellikleri arasında genişlik, yükseklik, x konumu, y konumu, döndürme ve daha fazlası bulunur. Geliştiriciler bunu kullanarak başarabilir[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).
### **Visio Şekil Korumasını düzenleyin**
**KilitAspect**, **Kilitle Başla**, **LockCalcWH**, **Kilit Kırpma**, **LockCustProp**, **KilitleSil**, **KilitSonu**, **Kilit Biçimi**, **LockFromGroupFormat**, **Kilit Grubu**, **Kilit Yüksekliği**, **KilitMoveX**, **LockMoveY**, **KilitleDöndür**, **Seçimi Kilitle**, **LockTextDüzenle**, **LockThemeColors**, **LockThemeEffects**, **LockVtxDüzenle** ve**Kilit Genişliği** maruz kalan özellikler[**Koruma**](https://reference.aspose.com/diagram/java/com.aspose.diagram/protection) sınıf desteği**Aspose.Diagram.BoolValue** nesne. Bu özellikler, şekilleri korumak ve korumayı kaldırmak için kullanılabilir.

Microsoft Office Visio'de kullanıcı herhangi bir şekli korumak için aşağıdaki işlemleri yapabilir:

- Açık diagram içinde Microsoft Office Visio
- Herhangi bir şekli seçin
- Visio 2007 kullanıyorsanız 'Format' menüsünden 'Koruma'yı, Visio 2010 kullanıyorsanız 'Geliştirici' menüsünden 'Koruma'yı seçin
- Herhangi bir şekil özelliğinin kilidini açmak için "Koruma" penceresinde herhangi bir metin kutusunun işaretini kaldırın.
- Tamam tuşuna basın'
### **Şekil Koruma Programlama Örneğinin Kaldırılması**
Aspose.Diagram for Java kullanarak aynı şeyi yapmak (herhangi bir şekil özniteliğinin kilidini açmak) için Java uygulamanızda aşağıdaki kodu kullanın.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VisioShapeProtection.class);
//Load diagram
Diagram diagram = new Diagram(dataDir + "ProtectAndUnprotect.vsd");
// get page by name
Page page = diagram.getPages().getPage("Flow 1");
// get shape by ID
Shape shape = page.getShapes().getShape(1);

// set protections
shape.getProtection().getLockAspect().setValue(BOOL.FALSE);
shape.getProtection().getLockBegin().setValue(BOOL.FALSE);
shape.getProtection().getLockCalcWH().setValue(BOOL.FALSE);
shape.getProtection().getLockCrop().setValue(BOOL.FALSE);
shape.getProtection().getLockCustProp().setValue(BOOL.FALSE);
shape.getProtection().getLockDelete().setValue(BOOL.FALSE);
shape.getProtection().getLockEnd().setValue(BOOL.FALSE);
shape.getProtection().getLockFormat().setValue(BOOL.FALSE);
shape.getProtection().getLockFromGroupFormat().setValue(BOOL.FALSE);
shape.getProtection().getLockGroup().setValue(BOOL.FALSE);
shape.getProtection().getLockHeight().setValue(BOOL.FALSE);
shape.getProtection().getLockMoveX().setValue(BOOL.FALSE);
shape.getProtection().getLockMoveY().setValue(BOOL.FALSE);
shape.getProtection().getLockRotate().setValue(BOOL.FALSE);
shape.getProtection().getLockSelect().setValue(BOOL.FALSE);
shape.getProtection().getLockTextEdit().setValue(BOOL.FALSE);
shape.getProtection().getLockThemeColors().setValue(BOOL.FALSE);
shape.getProtection().getLockThemeEffects().setValue(BOOL.FALSE);
shape.getProtection().getLockVtxEdit().setValue(BOOL.FALSE);
shape.getProtection().getLockWidth().setValue(BOOL.FALSE);
        
// save diagram
diagram.save(dataDir + "VisioShapeProtection_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

