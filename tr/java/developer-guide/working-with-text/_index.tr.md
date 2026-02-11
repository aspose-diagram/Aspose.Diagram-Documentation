---
title: Metinle Çalışmak
type: docs
weight: 120
url: /tr/java/working-with-text/
---
## **Visio Sayfasına Metin Şekli Ekleme**
 Aspose.Diagram API, geliştiricilerin Visio sayfasında herhangi bir yere bir metin şekli eklemesine olanak tanır. Bunu başarmak için, addText yöntemi[Sayfa](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) sınıf, PinX, PinY, genişlik, yükseklik ve metin parametrelerini alır.
### **Bir Metin Şekli Programlama Örneği Ekleme**
Aşağıdaki kod parçası, Visio diagram'de bir metin şekli ekler.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(InsertTextShape.class) + "Text/";
// create a new diagram
Diagram diagram = new Diagram();
// set parameters
double PinX = 1, PinY = 1, Width = 1, Height = 1;
String text = "Test text";
// add text to a Visio page
diagram.getPages().getPage(0).addText(PinX, PinY, Width, Height, text);
// save diagram 
diagram.save(dataDir + "InsertTextShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Güncelleme Visio Şekil Metni**
 Birlikte[diyagramlar oluşturma](/diagram/tr/java/load-or-create-a-visio-drawing/), Aspose.Diagram for Java, şekillerle farklı şekillerde çalışmanızı sağlar. Bu makalede, şekillerdeki metne nasıl erişileceği ve bu metnin nasıl güncelleneceği ele alınmaktadır.

 Tarafından sunulan Text özelliği[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) sınıfı, Aspose.Diagram.Text nesnesini destekler. Özellik, bir şeklin metnini almak veya güncellemek için kullanılabilir.

**Giriş diagram** 

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/6aEp7h0.png)

**Diagram, merkezi şekildeki metin İşlem'den Yeni Metin'e değiştirildikten sonra** 

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/o977cxw.png)

Bir şeklin metnini güncelleme işlemi basittir:

1. diagram yükleyin.
1. Belirli bir şekil bulun.
1. Yeni metni ayarlayın.
1. diagram'i kaydedin.
### **Shape Text Programlama Örneği Güncelleme**
Aşağıdaki kod parçası bir şeklin metnini günceller. Şekiller kimlikleri ile tanımlanır. Aşağıdaki kod parçaları, işlem adı verilen ve kimliği 1 olan bir şekli arar ve metnini değiştirir.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(UpdateShapeText.class); 
//Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "UpdateShapeText.vsd");
// get page by name
Page page = diagram.getPages().getPage("Flow 1");
//Find a particular shape and update its text
for (Shape shape :(Iterable<Shape>) page.getShapes())
{
    if (shape.getNameU().toLowerCase() == "process" && shape.getID() == 1)
    {
        shape.getText().getValue().clear();
        shape.getText().getValue().add(new Txt("New Text"));
    }
}
// save diagram
diagram.save(dataDir + "UpdateShapeText_Out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

## **Visio Şekline Yerleşik veya Özel Stil Sayfası Uygulayın**
Microsoft Visio stil sayfaları, tutarlı bir görünüm ve his için şekillere uygulanabilen biçimlendirme bilgilerini saklar. Aspose.Diagram for Java, bir uygulamanın içinden stil sayfaları uygulamanıza olanak tanır.

 tarafından sunulan TextStyle, FillStyle ve LineStyle özellikleri[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) sınıf desteği[Aspose.Diagram.StyleSheet](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/stylesheet) nesne. Özellik, stil bilgilerini almak ve bir diagram'e özel metin, çizgi ve dolgu stilleri uygulamak için kullanılabilir.

**Giriş diagram** 

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/feV1x2N.png)

**Metin, çizgi ve dolgu stillerini tanımlayan özel bir stil sayfası uygulandıktan sonra diagram** 

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/Xk9W0wN.png)
### **Microsoft Visio'deki Özel Stiller**
Microsoft Visio'deki şekillere özel stiller uygulamak için:

1. Microsoft Visio'de bir diagram açın.
1.  Seçme**Stilleri Tanımla** dan**Biçim** menüsü (Visio 2007) veya sağ tıklayın**stiller** içinde**Çizim Gezgini** penceresini açın ve seçin**Stilleri Tanımla** (Visio 2010).
1.  İçinde**Stilleri Tanımla** iletişim kutusunda, özel stil sayfanız için yeni bir ad yazın. Örneğin, CustomStyle1.
1.  Tıkla**Metin**, **Astar** ve**Doldurmak** Sırasıyla metin, çizgi ve dolgu stillerini ayarlamak için düğmeler.
1.  Tıklamak**TAMAM**.

Microsoft Visio'de özel stil sayfaları tanımladıktan sonra, şekillerinize özel stiller uygulamak için bir Java uygulamasında aşağıdaki kodu kullanın. Aşağıdaki kod örneklerinin yukarıda tanımlanan özel stil sayfasını çağırdığını unutmayın: uyguladığınız sayfanın adını ve konumunu bilmeniz gerekir.

Özel stilleri programlı olarak uygulamak için:

1. diagram yükleyin.
1. Stil uygulamak istediğiniz şekli bulun.
1. Stil sayfasını yükleyin.
1. Stilleri uygulayın.
1. diagram'i kaydedin.
#### **Özel Stiller Programlama Örneği Uygula**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ApplyCustomStyleSheets.class);

//Load diagram
Diagram diagram = new Diagram(dataDir + "ApplyCustomStyleSheets.vsd");
Shape sourceShape = null;
        
// get page by name
Page page = diagram.getPages().getPage("Flow 1");
//Find the shape that you want to apply style to
for (com.aspose.diagram.Shape shape : (Iterable<Shape>) page.getShapes())
{
    if (shape.getName() == "Process") {
        sourceShape = shape;
        break;
    }
}

StyleSheet customStyleSheet = null;

//Find the required style sheet
for (StyleSheet styleSheet : (Iterable<StyleSheet>) diagram.getStyleSheets())
{
    if (styleSheet.getName() == "CustomStyle1")
    {
        customStyleSheet = styleSheet;
        break;
    }
}

if (sourceShape != null && customStyleSheet != null)
{
    //Apply text style
    sourceShape.setTextStyle(customStyleSheet);
    //Apply fill style
    sourceShape.setFillStyle(customStyleSheet);
    //Apply line style
    sourceShape.setLineStyle(customStyleSheet);
}

 //Save the changed diagram as VDX
diagram.save(dataDir + "ApplyCustomStyleSheets_Out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

## **Bir Şeklin Her Metin Değerine Farklı Stil Uygulayın**
 Birlikte[diyagramlar oluşturma](/diagram/tr/java/load-or-create-a-visio-drawing/), Aspose.Diagram for Java, şekillerle farklı şekillerde çalışmanızı sağlar. Bu makale, bir şekle birden çok metin değeri eklemeye ve her metin değerine farklı stil uygulamaya yardımcı olur.

{{% alert color="primary" %}} 

Shape öğesi, metnin karakterlerini ve bir çalıştırmanın sonunu ve sonrakinin başlangıcını işaretleyen özel öğeleri (cp, pp, tp ve fld) içeren Metin adlı bir öğe içerir. Karakter Öğesi, şeklin metni için yazı tipi, renk, metin stili, büyük/küçük harf, taban çizgisine göre konum ve punto boyutu gibi biçimlendirme niteliklerini içerir.

{{% /alert %}} 
### **Şekil Metni ve Stilleri Ekleme**
**Giriş diagram** 

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/ZqgQPQC.png)

**Diagram her metin değerinde farklı stile sahip bir şekle çeşitli metin değerleri ekledikten sonra** 

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/7UWhFbU.png)
#### **Metin ve Stiller Programlama Örneği Ekleme**
Aşağıdaki kod parçası, bir şeklin metnini ve farklı stilleri ekler.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ApplyFontOnText.class);   
        
// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// get page by name
Page page = diagram.getPages().getPage("Page-1");
// get shape by ID
Shape shape = page.getShapes().getShape(1);
// clear shape text values and chars
shape.getText().getValue().clear();
shape.getChars().clear();

// mark character run and add text
shape.getText().getValue().add(new Cp(0));
shape.getText().getValue().add(new Txt("TextStyle_Regular\n"));
shape.getText().getValue().add(new Cp(1));
shape.getText().getValue().add(new Txt("TextStyle_Bold_Italic\n"));
shape.getText().getValue().add(new Cp(2));
shape.getText().getValue().add(new Txt("TextStyle_Underline_Italic\n"));
shape.getText().getValue().add(new Cp(3));
shape.getText().getValue().add(new Txt("TextStyle_Bold_Italic_Underline"));

// add formatting characters
shape.getChars().add(new Char());
shape.getChars().add(new Char());
shape.getChars().add(new Char());
shape.getChars().add(new Char());

//set properties e.g. color, font, size and style etc.
shape.getChars().get(0).setIX(0);
shape.getChars().get(0).getColor().setValue("#FF0000");
shape.getChars().get(0).getFont().setValue(1);
shape.getChars().get(0).getSize().setValue(0.22);
shape.getChars().get(0).getStyle().setValue(StyleValue.UNDEFINED);

//set properties e.g. color, font, size and style etc.
shape.getChars().get(1).setIX(1);
shape.getChars().get(1).getColor().setValue("#FF00FF");
shape.getChars().get(1).getFont().setValue(1);
shape.getChars().get(1).getSize().setValue(0.22);
shape.getChars().get(1).getStyle().setValue(StyleValue.BOLD | StyleValue.ITALIC);

//set properties e.g. color, font, size and style etc.
shape.getChars().get(2).setIX(2);
shape.getChars().get(2).getColor().setValue("#00FF00");
shape.getChars().get(2).getFont().setValue(1);
shape.getChars().get(2).getSize().setValue(0.22);
shape.getChars().get(2).getStyle().setValue(StyleValue.UNDERLINE | StyleValue.ITALIC);

//set properties e.g. color, font, size and style etc.
shape.getChars().get(3).setIX(3);
shape.getChars().get(3).getColor().setValue("#3333FF");
shape.getChars().get(3).getFont().setValue(1);
shape.getChars().get(3).getSize().setValue(0.22);
shape.getChars().get(3).getStyle().setValue(StyleValue.BOLD | StyleValue.ITALIC | StyleValue.UNDERLINE);
// save diagram
diagram.save(dataDir + "ApplyFontOnText_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Bir Şeklin Metnini Bul ve Değiştir**
 bu[Txt](https://reference.aspose.com/diagram/java/com.aspose.diagram/txt) Class, şeklin metnini düzenlemenizi sağlar. Tarafından sunulan replace yöntemi[Txt](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/txt) sınıf, bir şeklin metnini değiştirmeyi destekler.
Bu makaledeki kod örnekleri, sayfadaki şeklin metnini bulur ve değiştirir.

**Giriş diagram** 

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/lW5xaP0.png)


**Şekil düzenlendikten sonra diagram** 

![yapılacaklar:resim_alternatif_Metin](http://i.imgur.com/m33W1Tk.png)

Şeklin metnini değiştirme süreci:

1. diagram yükleyin.
1. Bir şeklin belirli bir metnini bulun.
1. Bu şeklin metnini değiştir
1. diagram'i kaydedin.
### **Metin Programlama Örneği Bul ve Değiştir**
Aşağıdaki kod parçacıkları, şeklin metninin nasıl değiştirileceğini gösterir. Kod, bir sayfanın şekillerini yineler.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(FindAndReplaceShapeText.class); 
// load diagram
Diagram diagram = new Diagram(dataDir + "FindReplaceText.vsdx");

DateFormat dateFormat = new SimpleDateFormat("dd/MMMM/yyyy");
Date myDate = new Date(System.currentTimeMillis());
Calendar cal = Calendar.getInstance();

// Prepare a collection old and new text
Hashtable<String, String> replacements = new Hashtable<String, String>();
replacements.put("[[CompanyName]]", "Research Society of XYZ");
replacements.put("[[CompanyName]]", "Research Society of XYZ");
replacements.put("[[EmplyeeName]]", "James Bond");
replacements.put("[[SubjectTitle]]", "The affect of the internet on social behavior in the industrialize world");

cal.setTime(myDate);
cal.add(Calendar.YEAR, -1);
System.out.println(dateFormat.format(cal.getTime()));
replacements.put("[[TimePeriod]]", dateFormat.format(cal.getTime()) + " -- " + dateFormat.format(myDate));

cal.setTime(myDate);
cal.add(Calendar.DAY_OF_MONTH, -7);
System.out.println(dateFormat.format(cal.getTime()));
replacements.put("[[SubmissionDate]]", dateFormat.format(cal.getTime()));
replacements.put("[[AmountReq]]", "$100,000");

cal.setTime(myDate);
cal.add(Calendar.DAY_OF_MONTH, 1);
System.out.println(dateFormat.format(cal.getTime()));
replacements.put("[[DateApproved]]", dateFormat.format(cal.getTime()));

// Iterate through the shapes of a page
for (Shape shape : (Iterable<Shape>) diagram.getPages().getPage("Page-1").getShapes())
{
    Set<String> keys = replacements.keySet();
    for(String key: keys)
    {
        for (FormatTxt txt : (Iterable<FormatTxt>) shape.getText().getValue())
        {
       	    Txt tx = (Txt)((txt instanceof Txt) ? txt : null);
            if (tx != null && tx.getText().contains(key))
            {
                //find and replace text of a shape
                tx.setText(tx.getText().replace(key, replacements.get(key)));
            }
        }
    }
}
// Save the diagram
diagram.save(dataDir + "FindAndReplaceShapeText_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Visio Diagram Sayfasından Düz Metni Çıkarın**
Aspose.Diagram API, geliştiricilerin Visio diagram sayfasından düz metin çıkarmasına olanak tanır. Ayrıca Visio diagram metninin tamamını kapsayacak şekilde Visio diagram sayfalarını yineleyebilirler.

 Microsoft Office Visio yazıları şekillere ekliyor. bu[Şekil](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape) class, metnin karakterlerini ve bir çalıştırmanın sonunu ve sonrakinin başlangıcını işaretleyen özel öğeleri (cp, pp, tp ve fld) içeren Metin adlı bir öğe içerir.
### **Düz Metin Programlama Örneği Çıkarın**
Aşağıdaki kod parçası, Visio Sayfasının şekillerini yineler ve biçimlendirme bilgisi olmadan düz metni filtreler.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
static String text = "";
public static void main(String[] args) throws Exception
{
       // The path to the documents directory.
       String dataDir = Utils.getDataDir(GetPlainTextOfVisio.class);
       // load diagram
       Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

       // get Visio diagram page
       Page page = diagram.getPages().getPage("Page-1");

       // iterate through the shapes
       for (Shape shape :(Iterable<Shape>) page.getShapes())
       {
           // extract plain text from the shape
           GetShapeText(shape);
       }
       // display extracted text
       System.out.println(text);
}
   private static void GetShapeText(Shape shape)
   {
   	// filter shape text
       if (shape.getText().getValue().getText() != "")
       	text += (shape.getText().getValue().getText().replaceAll("\\<.*?>",""));

       // for image shapes
       if (shape.getType() == TypeValue.FOREIGN)
           text += (shape.getName());

       // for group shapes
       if (shape.getType() == TypeValue.GROUP)
           for(Shape subshape : (Iterable<Shape>) shape.getShapes())
           {
               GetShapeText(subshape);
           }
   }

{{< /highlight >}}

